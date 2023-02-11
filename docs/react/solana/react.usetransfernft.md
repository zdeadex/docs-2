---
slug: /solana/react.usetransfernft
title: useTransferNFT
hide_title: true
displayed_sidebar: react
---
<!-- Do not edit this file. It is automatically generated by API Documenter. -->


# useTransferNFT

Transfer NFTs from the connected wallet to another wallet

## Example


```jsx
import { useProgram, useTransferNFT } from "@thirdweb-dev/react/solana";

export default function Component() {
  const { program } = useProgram("{{program_address}}");
  const { mutateAsync: transfer, isLoading, error } = useTransferNFT(program);

  return (
    <button
      onClick={() => transfer({
        receiverAddress: "{{wallet_address}}",
        tokenAddress: "..."
      })}
    >
      Transfer
    </button>
  )
}
```

**Signature:**

```typescript
export declare function useTransferNFT(program: RequiredParam<NFTCollection | NFTDrop>): import("@tanstack/react-query").UseMutationResult<import("@thirdweb-dev/sdk/solana").TransactionResult, unknown, TransferNFTMutationParams, unknown>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  program | [RequiredParam](./react.requiredparam.md)&lt;NFTCollection &#124; NFTDrop&gt; | The NFT program instance to transfer NFTs on |

**Returns:**

import("@tanstack/react-query").UseMutationResult&lt;import("@thirdweb-dev/sdk/solana").TransactionResult, unknown, [TransferNFTMutationParams](./react.transfernftmutationparams.md), unknown&gt;