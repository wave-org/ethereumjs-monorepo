[@ethereumjs/common](../README.md) / CommonOpts

# Interface: CommonOpts

Options for instantiating a [Common](../classes/Common.md) instance.

## Hierarchy

- `BaseOpts`

  ↳ **`CommonOpts`**

## Table of contents

### Properties

- [chain](CommonOpts.md#chain)
- [customChains](CommonOpts.md#customchains)
- [eips](CommonOpts.md#eips)
- [hardfork](CommonOpts.md#hardfork)

## Properties

### chain

• **chain**: `string` \| `number` \| `bigint` \| `object`

Chain name ('mainnet'), id (1), or [Chain](../enums/Chain.md) enum,
either from a chain directly supported or a custom chain
passed in via [customChains](CommonOpts.md#customchains).

#### Defined in

[types.ts:90](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/common/src/types.ts#L90)

___

### customChains

• `Optional` **customChains**: [`ChainConfig`](ChainConfig.md)[]

Initialize (in addition to the supported chains) with the selected
custom chains. Custom genesis state should be passed to the Blockchain class if used.

Usage (directly with the respective chain initialization via the [chain](CommonOpts.md#chain) option):

```javascript
import myCustomChain1 from '[PATH_TO_MY_CHAINS]/myCustomChain1.json'
const common = new Common({ chain: 'myCustomChain1', customChains: [ myCustomChain1 ]})
```

#### Defined in

[types.ts:102](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/common/src/types.ts#L102)

___

### eips

• `Optional` **eips**: `number`[]

Selected EIPs which can be activated, please use an array for instantiation
(e.g. `eips: [ 1559, 3860 ]`)

#### Inherited from

BaseOpts.eips

#### Defined in

[types.ts:78](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/common/src/types.ts#L78)

___

### hardfork

• `Optional` **hardfork**: `string`

String identifier ('byzantium') for hardfork or [Hardfork](../enums/Hardfork.md) enum.

Default: Hardfork.London

#### Inherited from

BaseOpts.hardfork

#### Defined in

[types.ts:73](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/common/src/types.ts#L73)
