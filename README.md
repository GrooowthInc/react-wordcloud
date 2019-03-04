# ☁️ React Wordcloud

Simple React + D3 wordcloud component with powerful features. Uses the [`d3-cloud`](https://github.com/jasondavies/d3-cloud) layout.

![image](./wordcloud.png)

## Install

```bash
yarn add https://github.com/chrisrzhou/react-wordcloud.git
```

Note that `react-wordcloud` requires `react^16.8.3` as a peer dependency.

## Examples

View all documented examples at https://chrisrzhou.github.io/wordcloud/

A simple example using only required props:

```js
import * as React from "react";
import ReactWordcloud from "react-wordcloud";

const words = [
  { text: "hello", count: 3 },
  { text: "world", count: 1 },
  { text: "github", count: 1 },
  { text: "code", count: 1 }
];

function MyApp() {
  return (
    <div style={{ width: 600, height: 400 }}>
      <ReactWordcloud words={words} />
    </div>
  );
}
```

You can also run the examples locally:

```bash
git clone git@github.com:chrisrzhou/react-wordcloud

cd react-wordcloud
yarn
yarn dev
```

## Development

### Main Dependencies

- `react`
- `d3`
- `d3-cloud`
- `tippy.js`

### Codebase Overview

- `index.tsx`: Pure React code that exposes an interface of props. Tooltip and cloud layout is also configured here.
- `render.ts`: Pure D3 rendering code when a D3 selection and other data are provided.
- `hooks.ts`: React hooks that build and destroy responsive SVG containers with D3.
- `types.ts`: Typescript types.
- `utils.ts`: Various simple functions used to compute derived data.

The code is written in `typescript`, linted with `eslint` + `prettier`, and built with `rollup`. Examples and documentations are built with `docz`.

Feel free to contribute by submitting a pull request.

## Wordcloud Generator

Create wordclouds using this wordcloud generator: https://chrisrzhou.github.io/wordcloud-generator/

Features supported:

- Editing and uploading text inputs
- Various NLP methods (stopwords, ngrams)
- Wordcloud configurations
- Export/save/share wordclouds
