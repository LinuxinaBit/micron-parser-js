Micron Parser JS
-
This repository provides a JavaScript parser for Micron, a lightweight, terminal-friendly markdown format used
in  [NomadNet](https://github.com/markqvist/NomadNet) and [MeshChat](https://github.com/liamcottle/reticulum-meshchat)

## Usage

```js
// Import Micron Parser (requires modules)
import MicronParser from './js/micron-parser.js';

// Create a new parser (darkTheme = true/false | defaults to true, forceMonospace = true/false | defaults to true)
const parser = new MicronParser(true, true);

// Input Micron markup
const micronMarkup = `
> Example Heading
-∿
This is a simple line in Micron.
# This line is a comment and won't appear in the output.
`;

// Convert Micron to an HTML string
const htmlOutput = parser.convertMicronToHtml(micronMarkup);

// Insert it into your page
document.getElementById('yourElement').innerHTML = htmlOutput;

// Or create a DocumentFragment from Micron
const domFragment = parser.convertMicronToFragment(micronMarkup);
// and append it to the DOM
document.body.appendChild(domFragment);
```

## Best practices

For optimal display of Micron content in the browser it's recommended to use a monospaced font with NerdFont icon support, such as the ones provided [here](https://www.nerdfonts.com/font-downloads).  


