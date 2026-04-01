# tree-sitter-jsp

JSP (JavaServer Pages) grammar for [tree-sitter](https://github.com/tree-sitter/tree-sitter).

## Features

- JSP directives (`<%@ ... %>`)
- Declarations (`<%! ... %>`)
- Scriptlets (`<% ... %>`)
- Expressions (`<%= ... %>`)
- Comments (`<%-- ... --%>`)
- Expression Language (`${...}` and `#{...}`)
- Language injection queries for Java code blocks and HTML content

## Usage

### Swift (SPM)

Add the package as a dependency in your `Package.swift`:

```swift
dependencies: [
    .package(url: "https://github.com/karlvr/tree-sitter-jsp", from: "0.1.0"),
]
```

Then add it to your target's dependencies:

```swift
.product(name: "TreeSitterJSP", package: "tree-sitter-jsp"),
```

Use the parser:

```swift
import TreeSitterJSP
import SwiftTreeSitter

let language = Language(tree_sitter_jsp())
```

### Node.js

```sh
npm install tree-sitter tree-sitter-jsp
```

```javascript
const Parser = require("tree-sitter");
const JSP = require("tree-sitter-jsp");

const parser = new Parser();
parser.setLanguage(JSP);

const tree = parser.parse("<%= request.getParameter(\"name\") %>");
console.log(tree.rootNode.toString());
```

## Developing

### Building

```sh
npm install
npm run build
```

### Testing

```sh
npm test
```

## References

- [JSP Specification](https://jakarta.ee/specifications/pages/)
- [Expression Language Specification](https://jakarta.ee/specifications/expression-language/)

## License

MIT
