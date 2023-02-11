---
slug: /solana/react.usedropunclaimedsupply
title: useDropUnclaimedSupply
hide_title: true
displayed_sidebar: react
---
<!-- Do not edit this file. It is automatically generated by API Documenter. -->


# useDropUnclaimedSupply

Get the total unclaimed supply of NFTs on an NFT Drop

## Example


```jsx
import { useProgram, useDropTotalUnclaimedSupply } from "@thirdweb-dev/react/solana";

export default function Component() {
  const { program } = useProgram("{{program_address}}");
  const { data: unclaimedSupply, isLoading } = useDropTotalUnclaimedSupply(program);

  return (
    <p>{unclaimedSupply}</p>
  )
}
```

**Signature:**

```typescript
export declare function useDropUnclaimedSupply(program: RequiredParam<NFTDrop>): import("@tanstack/react-query").UseQueryResult<number, unknown>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  program | [RequiredParam](./react.requiredparam.md)&lt;NFTDrop&gt; | The NFT Drop program to get the unclaimed supply on |

**Returns:**

import("@tanstack/react-query").UseQueryResult&lt;number, unknown&gt;