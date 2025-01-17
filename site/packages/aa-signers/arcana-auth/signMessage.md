---
outline: deep
head:
  - - meta
    - property: og:title
      content: ArcanaAuthSigner • signMessage
  - - meta
    - name: description
      content: Overview of the signMessage method on ArcanaAuthSigner
  - - meta
    - property: og:description
      content: Overview of the signMessage method on ArcanaAuthSigner
---

# signMessage

`signMessage` supports signing messages from the `ArcanaAuthSigner`.

This method must be called after [`authenticate`](/packages/aa-signers/arcana-auth/authenticate). Otherwise, this method will throw an error with the message `Not Authenticated`.

## Usage

::: code-group

```ts [example.ts]
import { createArcanaAuthSigner } from "./arcana-auth";
// [!code focus:99]
const newArcanaAuthSigner = await createArcanaAuthSigner();

const signedMessage = await newArcanaAuthSigner.signMessage(
  "testMessage signing with ArcanaAuthSigner"
);
```

<<< @/snippets/arcana-auth.ts
:::

## Returns

### `Promise<Hex>`

A Promise containing the signature of the message.

## Parameters

### `msg: string | Uint8Array)` -- the message to sign
