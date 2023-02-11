---
slug: /react.usetotalcount
title: useTotalCount
hide_title: true
displayed_sidebar: react
---
<!-- Do not edit this file. It is automatically generated by API Documenter. -->


# useTotalCount

> This feature is currently in beta and may change based on feedback that we receive.
> 

Use this to get the total count of NFT tokens of your [NFTContract](./react.nftcontract.md).

## Example


```javascript
const { contract } = useContract(<ContractAddress>);
const { data: count, isLoading, error } = useTotalCount(contract);
```

**Signature:**

```typescript
export declare function useTotalCount<TContract extends NFTContract>(contract: RequiredParam<TContract>): import("@tanstack/react-query").UseQueryResult<BigNumber, unknown>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  contract | [RequiredParam](./react.requiredparam.md)&lt;TContract&gt; | an instance of a [NFTContract](./react.nftcontract.md) |

**Returns:**

import("@tanstack/react-query").UseQueryResult&lt;BigNumber, unknown&gt;

a response object that includes the total count of NFTs