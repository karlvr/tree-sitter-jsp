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

### Node.js

```sh
npm install tree-sitter-jsp
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
