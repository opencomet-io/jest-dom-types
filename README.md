# jest-dom-types

This package contains type definitions for `@testing-library/jest-dom`.

This package is forked from `@types/testing-library__jest-dom`,
this version does not have `@types/jest` as dependency,
which can be useful for usage with [Vitest](https://github.com/vitest-dev/vitest).

## Usage with Vitest

Add this to your `package.json` if you're using Yarn:

```json
{
  // ...
  "resolutions": {
    "@types/testing-library__jest-dom": "opencomet-io/jest-dom-types"
  }
}
```

Your test setup file (e.g. `test/setup.ts`) should look like this:

```ts
import '@testing-library/jest-dom';
import matchers from '@testing-library/jest-dom/matchers';
import { expect } from 'vitest';

expect.extend(matchers);
```

## Credits

These definitions were written by [Ernesto García](https://github.com/gnapse), [John Gozde](https://github.com/jgoz), [Seth Macpherson](https://github.com/smacpherson64), and [Andrew Leedham](https://github.com/AndrewLeedham).

## License

MIT
