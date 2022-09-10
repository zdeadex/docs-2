---
slug: /react.usetokendecimals
title: useTokenDecimals() function
hide_title: true
displayed_sidebar: react
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

## useTokenDecimals() function

> This feature is currently in beta and may change based on feedback that we receive.

Use this to get the decimals of your contract for a given address.

## Example

```javascript
const { data: decimals, isLoading, error } = useTokenDecimals(<YourTokenContractInstance>);
```

**Signature:**

```typescript
export declare function useTokenDecimals(
  contract: RequiredParam<Erc20>,
): import("@tanstack/react-query").UseQueryResult<number, unknown>;
```

## Parameters

| Parameter | Type                                                   | Description                       |
| --------- | ------------------------------------------------------ | --------------------------------- |
| contract  | [RequiredParam](./react.requiredparam.md)&lt;Erc20&gt; | an instance of an ERC20 contract. |

**Returns:**

import("@tanstack/react-query").UseQueryResult&lt;number, unknown&gt;

a response object that includes the decimals of the ERC20 token