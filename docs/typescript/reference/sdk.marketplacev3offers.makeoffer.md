---
slug: /reference/sdk.marketplacev3offers.makeoffer
title: MarketplaceV3Offers.makeOffer property
hide_title: true
displayed_sidebar: typescript
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

# MarketplaceV3Offers.makeOffer property

Make an offer

## Example

```javascript
// Data of the offer you want to make
const offer = {
  // address of the contract the asset you want to make an offer for
  assetContractAddress: "0x...",
  // token ID of the asset you want to buy
  tokenId: "0",
  // how many of the asset you want to buy
  quantity: 1,
  // address of the currency contract that you offer to pay in
  currencyContractAddress: NATIVE_TOKEN_ADDRESS,
  // Total price you offer to pay for the mentioned token(s)
  totalPrice: "1.5",
  // Offer valid until
  endTimestamp: new Date(),
};

const tx = await contract.offers.makeOffer(offer);
const receipt = tx.receipt; // the transaction receipt
const id = tx.id; // the id of the newly created offer
```

**Signature:**

```typescript
makeOffer: {
        (offer: {
            tokenId: (string | number | bigint | BigNumber) & (string | number | bigint | BigNumber | undefined);
            totalPrice: string | number;
            assetContractAddress: string;
            quantity?: string | number | bigint | BigNumber | undefined;
            currencyContractAddress?: string | undefined;
            endTimestamp?: Date | undefined;
        }): Promise<TransactionResultWithId<never>>;
        prepare: (offer: {
            tokenId: (string | number | bigint | BigNumber) & (string | number | bigint | BigNumber | undefined);
            totalPrice: string | number;
            assetContractAddress: string;
            quantity?: string | number | bigint | BigNumber | undefined;
            currencyContractAddress?: string | undefined;
            endTimestamp?: Date | undefined;
        }) => Promise<Transaction<TransactionResultWithId<never>>>;
    };
```

## Remarks

Make an offer on the marketplace for an asset.