---
slug: /solana/react.useupdatecreators
title: useUpdateCreators
hide_title: true
displayed_sidebar: react
---
<!-- Do not edit this file. It is automatically generated by API Documenter. -->


# useUpdateCreators

Update the creators for an NFT program

## Example


```jsx
import { useProgram, useUpdateCreators } from "@thirdweb-dev/react/solana";

export default function Component() {
  const { program } = useProgram("{{program_address}}");
  const { mutateAsync: updateCreators, isLoading, error } = useUpdateCreators(program);

  return (
    <button
      onClick={() => updateCreators([{ address: "0x...", share: 10 }])}
    >
      Update Creators
    </button>
  )
}
```

**Signature:**

```typescript
export declare function useUpdateCreators(program: RequiredParam<NFTCollection | NFTDrop>): import("@tanstack/react-query").UseMutationResult<import("@thirdweb-dev/sdk/solana").TransactionResult[], unknown, UpdateCreatorInput, unknown>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  program | [RequiredParam](./react.requiredparam.md)&lt;NFTCollection &#124; NFTDrop&gt; | The NFT program instance to update the creators for |

**Returns:**

import("@tanstack/react-query").UseMutationResult&lt;import("@thirdweb-dev/sdk/solana").TransactionResult\[\], unknown, UpdateCreatorInput, unknown&gt;