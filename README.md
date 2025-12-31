# Monaco Editor

[![Versions](https://img.shields.io/npm/v/monaco-editor)](https://www.npmjs.com/package/monaco-editor)
[![Versions](https://img.shields.io/npm/v/monaco-editor/next)](https://www.npmjs.com/package/monaco-editor)
[![Feature Requests](https://img.shields.io/github/issues/microsoft/monaco-editor/feature-request.svg)](https://github.com/microsoft/monaco-editor/issues?q=is%3Aopen+is%3Aissue+label%3Afeature-request+sort%3Areactions-%2B1-desc)
[![Bugs](https://img.shields.io/github/issues/microsoft/monaco-editor/bug.svg)](https://github.com/microsoft/monaco-editor/issues?utf8=✓&q=is%3Aissue+is%3Aopen+label%3Abug)

The Monaco Editor is the fully featured code editor from [VS Code](https://github.com/microsoft/vscode). Check out the [VS Code docs](https://code.visualstudio.com/docs/editor/editingevolved) to see some of the supported features.

![image](https://user-images.githubusercontent.com/5047891/94183711-290c0780-fea3-11ea-90e3-c88ff9d21bd6.png)

## Try it out

Try out the editor and see various examples [in our interactive playground](https://microsoft.github.io/monaco-editor/playground.html).

The playground is the best way to learn about how to use the editor, which features is supports, to try out different versions and to create minimal reproducible examples for bug reports.

## Installing

```
> npm install monaco-editor
```

You will get:

- inside `/esm`: ESM version of the editor (compatible with e.g. webpack)
- `monaco.d.ts`: this specifies the API of the editor (this is what is actually versioned, everything else is considered private and might break with any release).

:warning: The monaco editor also ships an `AMD` build for backwards-compatibility reasons, but the `AMD` support is deprecated and will be removed in future versions.

## Localization

To load the editor in a specific language, make sure that the corresponding nls script file is loaded before the main monaco editor script. For example, to load the editor in German, include the following script tag:
```html
<script src="path/to/monaco-editor/esm/nls.messages.de.js"></script>
```

Check the sources for available languages.

## Concepts

Monaco editor is best known for being the text editor that powers VS Code. However, it's a bit more nuanced. Some basic understanding about the underlying concepts is needed to use Monaco editor effectively.

### Models

Models are at the heart of Monaco editor. It's what you interact with when managing content. A model represents a file that has been opened. This could represent a file that exists on a file system, but it doesn't have to. For example, the model holds the text content, determines the language of the content, and tracks the edit history of the content.


