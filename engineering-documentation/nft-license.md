---
description: >-
  Node operators, hardware manufacturers, etc. can stake $DIMO to mint a
  license.
---

# NFT License

![Overview ](https://user-images.githubusercontent.com/5941389/183465383-06fd38ca-84fd-42ad-8063-878190dd6eba.png)

## License NFT (Account Bound Tokens)

The original idea for soulbound tokens comes from [Vitalik Butterin](https://vitalik.ca/general/2022/01/26/soulbound.html). There is no official spec nor EIP for soulbound tokens, but there are several implementations with different trade offs.

#### **Design Decisions**

We had some requirements to consider for Licensing

* Keep pushing towards a web3/decentralized ecosystem
* Prevent manufacturers from minting infinite licenses
* Track the issuances of licenses
* Easier onboarding of future Manufacturers
* Include specific metadata to prevent abuse

In order to deliver the functionality inachieve the diagram above, where Hardware Manufacturers are licensed to create new DIMO-enabled devices we heavily influenced by Account Bound Tokens (EIP-4973).

### Advantages of ABTs

Soulbound tokens override the `ERC721`'s transfer function to revert. This allows for the user to hold a token indefinitely, but it also binds the asset to the user's private key. If a user or institution loses access to their wallet, that asset is permanently unrecoverable. However, with an ABT, the token can be revoked and reassigned (granted they prove their identity/ownership first).

There may be a situation in which an attacker gains access to a SBT and is able to take out a loan in their name for example, whereas this situation can be mitigated with an ABT by simply revoking access.

Additionally, there is a planned feature for `EIP4973` to include a `mintWithPermit()` function which would allow for "lazy minting" an ABT with the implementer's signed permission.

### Interfaces

In order to be maximally backward-compatible with existing ERC721 Infrastructure, ABTs (Account Bound Tokens) implement existing functions purposefully. Things like `EIP-165` and `ERC721Metadata` which wallets will already be familiar with.

Additionally there is a `checkUserIsWhiteListed(address user)` function that returns a boolean and checks to see that the user has staked greater than the `minStakeAmount` in order to return true.

### ERC165

the IERC165 Interface is a single function `supportsInterface()` with takes in a `bytes4 interfaceId` as the parameter. The interfaceId is the 8bit hex string for the calldata of the function. The purpose of this method is for a contract to "ask" a second contract if it supports a specific method. This prevents sending tokens to a contract that cannot read them. For example, sending an `ERC1155` token to an `ERC20` contract would leave them stuck.

By hashing the function name and it's parameters, you can use the result to check if the method is supported.

`keccak256("tokenByIndex(uint256)") == '0xasdfasdf"`

you would then do

`supportsInterface("0xasdfasdf")`

and the resulting boolean would tell you whether it's safe to proceed or not.

### Events

Our `License`has two main events;

**Attest**

```
(address indexed _to, uint256 indexed _tokenId);
```

Emits when a new token is related and bound to an account by any mechanism

**Revoke**

```
(address indexed _to, uint256 indexed _tokenId);
```

Emits when an existing ABT is revoked from an account and destroyed by any mechanism.

#### Fund recovery

In the event a user accidentally sends DIMO tokens directly to the contract, the tokens would not be credited to the sender and the tokens would effectively be “stuck” or “lost”. This is a limitation of the ERC20 standard and would apply to any token being sent to any smart contract.

To recover lost DIMO, we implemented a `emergencyWithdraw()` function that first checks for stuck tokens by subtracting the `dimoTotalAmountStaked` value from the total number of DIMO held on the contract. The returning value is only ever positive when the user accidentally sends tokens directly rather than interacting with the `stake()` function.

If there is a positive amount, and the user has a staked balance, the tokens are transferred to the specified user and the `EmergencyWithdrawal(user,amount)` event is emitted.

### Upgradeability

To implement future features for posterity, we are using the Universal Upgradeable Proxy Standard, aka [EIP 1822](https://eips.ethereum.org/EIPS/eip-1822). This pattern is a standard for proxy contracts which is universally compatible with all contracts, and does not create incompatibility between the proxy and business-logic contracts. This is achieved by utilizing a unique storage position in the proxy contract to store the Logic Contract’s address. A compatibility check ensures successful upgrades. Upgrading can be performed unlimited times, or as determined by custom logic. In addition, a method for selecting from multiple constructors is provided, which does not inhibit the ability to verify bytecode.
