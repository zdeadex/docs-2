---
slug: /react.usemakebid
title: useMakeBid
hide_title: true
displayed_sidebar: react
---
<!-- Do not edit this file. It is automatically generated by API Documenter. -->


# useMakeBid

> This feature is currently in beta and may change based on feedback that we receive.
> 

Use this to place a bid on an auction listing from your marketplace contract.

## Example


```jsx
const Component = () => {
  const {
    mutate: makeBid,
    isLoading,
    error,
  } = useMakeBid(">>YourMarketplaceContractInstance<<");

  if (error) {
    console.error("failed to make a bid", error);
  }

  return (
    <button
      disabled={isLoading}
      onClick={() => makeBid({ listingId: 1, bid: 2 })}
    >
      Bid!
    </button>
  );
};
```

**Signature:**

```typescript
export declare function useMakeBid(contract: RequiredParam<Marketplace>): import("@tanstack/react-query").UseMutationResult<Omit<{
    receipt: import("@ethersproject/abstract-provider").TransactionReceipt;
    data: () => Promise<unknown>;
}, "data">, unknown, MakeBidParams, unknown>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  contract | [RequiredParam](./react.requiredparam.md)&lt;Marketplace&gt; | an instance of a Marketplace contract |

**Returns:**

import("@tanstack/react-query").UseMutationResult&lt;Omit&lt;{ receipt: import("@ethersproject/abstract-provider").TransactionReceipt; data: () =&gt; Promise&lt;unknown&gt;; }, "data"&gt;, unknown, [MakeBidParams](./react.makebidparams.md), unknown&gt;

a mutation object that can be used to make a bid on an auction listing