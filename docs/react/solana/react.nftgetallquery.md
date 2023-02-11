---
slug: /solana/react.nftgetallquery
title: nftGetAllQuery
hide_title: true
displayed_sidebar: react
---
<!-- Do not edit this file. It is automatically generated by API Documenter. -->


# nftGetAllQuery

**Signature:**

```typescript
export declare function nftGetAllQuery(program: RequiredParam<NFTCollection | NFTDrop>, queryParams?: QueryAllParams): {
    queryKey: readonly ["__tw__", "sol", RequiredParam<import("@thirdweb-dev/sdk/solana").Network>, "program", string | undefined, "getAll", {
        start?: number | undefined;
        count?: number | undefined;
    } | undefined];
    queryFn: () => Promise<import("@thirdweb-dev/sdk").NFT[]>;
    enabled: boolean;
};
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  program | [RequiredParam](./react.requiredparam.md)&lt;NFTCollection &#124; NFTDrop&gt; |  |
|  queryParams | QueryAllParams | <i>(Optional)</i> |

**Returns:**

{ queryKey: readonly \["\_\_tw\_\_", "sol", [RequiredParam](./react.requiredparam.md)&lt;import("@thirdweb-dev/sdk/solana").Network&gt;, "program", string \| undefined, "getAll", { start?: number \| undefined; count?: number \| undefined; } \| undefined\]; queryFn: () =&gt; Promise&lt;import("@thirdweb-dev/sdk").NFT\[\]&gt;; enabled: boolean; }