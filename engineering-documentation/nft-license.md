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

In order to deliver the functionality inachieve the diagram above, where Hardware Manufacturers are licensed to create new DIMO-enabled devices we are using Account Bound Tokens (EIP-4973).

### Advantages of ABTs

Soulbound tokens override the `ERC721`'s transfer function to revert. This allows for the user to hold a token indefinitely, but it also binds the asset to the user's private key. If a user or institution loses access to their wallet, that asset is permanently unrecoverable. However, with an ABT, the token can be revoked and reassigned (granted they prove their identity/ownership first).

There may be a situation in which an attacker gains access to a SBT and is able to take out a loan in their name for example, whereas this situation can be mitigated with an ABT by simply revoking access.

Additionally, there is a planned feature for `EIP4973` to include a `mintWithPermit()` function which would allow for "lazy minting" an ABT with the implementer's signed permission.

### Interfaces

In order to be maximally backward-compatible with existing ERC721 Infrastructure, ABTs (Account Bound Tokens) implement existing functions purposefully. Things like `EIP-165` and `ERC721Metadata` which wallets will already be familiar with.

### ERC165

the IERC165 Interface is a single function `supportsInterface()` with takes in a `bytes4 interfaceId` as the parameter. The interfaceId is the 8bit hex string for the calldata of the function. The purpose of this method is for a contract to "ask" a second contract if it supports a specific method. This prevents sending tokens to a contract that cannot read them. For example, sending an `ERC1155` token to an `ERC20` contract would leave them stuck.

By hashing the function name and it's parameters, you can use the result to check if the method is supported.

`keccak256("tokenByIndex(uint256)") == '0xasdfasdf"`

you would then do

`supportsInterface("0xasdfasdf")`

and the resulting boolean would tell you whether it's safe to proceed or not.

### Events

`IERC4973` has two main events;

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
