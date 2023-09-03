# E2E Helpers

To make the process for writing e2e-tests less tricky and more comfortable
we have prepared a set of tools that will help you to focus on testing scenarios.

- [Q Helper](docs/QHelper.md) // Provides shortcuts for css-queries
- [R Helper](docs/RHelper.md) // Provides shortcuts for url-patterns

## Helpers

### Initialization
```ts
import { e2eHelpersFactory } from 'e2e-helpers';
export const { q, r } = e2eHelpersFactory(/* Config */);
```
or
```ts
import { e2eHelpersFactory } from 'e2e-helpers';
const { q, r } = e2eHelpersFactory(/* Config */);

global.q = q;
global.r = r;
```

### Configuration
#### Default config
```ts
const config = {
    customSelectorAttr: 'data-test-id',
    customSelectorParamAttrPrefix: 'data-test-',
    customSelectorPrefix: '%',
    pseudoSelectorPrefix: '%%',
    pseudoSelectorMap: {},
}
```
```ts
interface E2EHelpersConfig {
    customSelectorAttr: string
    customSelectorParamAttrPrefix: string
    customSelectorPrefix: string
    pseudoSelectorPrefix: string
    pseudoSelectorMap: Record<string, string>
}
```
