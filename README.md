# Astro Portal Component

A lightweight Astro component for rendering content in a different part of the DOM using a Web Component.

## Installation

```sh
npm install astro-teleport
```

or with Yarn:

```sh
yarn add astro-teleport
```

or with pnpm:

```sh
pnpm add astro-teleport
```

## Usage

### Basic Example

```astro
---
import Portal from "astro-teleport";
---

<Portal data-target="#modal" data-open={true}>
  <div>
    <h2>This is inside the portal!</h2>
  </div>
</Portal>
```

## Props

| Prop         | Type    | Description                                            |
|-------------|--------|--------------------------------------------------------|
| `data-target` | `string` | A CSS selector for the target container. Defaults to `body`. |
| `data-open`  | `boolean` | Controls whether the portal content is shown.         |

## How It Works

- The `Portal` component moves its children to the specified `data-target` element.
- If `data-target` is not provided, it defaults to `document.body`.
- When `data-open` is `true`, the portal content is mounted inside the target.
- When `data-open` is `false`, the content is removed from the target.


## License

MIT

