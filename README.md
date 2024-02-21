# tiptap-clean-paste

The Tiptap Clean Paste Extension is a plugin for [Tiptap](https://tiptap.dev/) that provides a clean paste functionality for your editor. It allows you to strip unwanted content from pasted text, such as formatting, styles, or non-printable characters.

## Installation

You can install the Tiptap Clean Paste Extension via npm:

```bash
npm install tiptap-clean-paste
```

## Installation

To use the tiptap-clean-paste Extension in your Tiptap editor, import it and add it to your extensions list:

```jsx
import { CleanPaste } from "tiptap-clean-paste";
// or
import CleanPaste from "tiptap-clean-paste";

// Using the default regex pattern
const extensions = [CleanPasteExtension];

// Or define your custom regex pattern
const customRegex = /[^\x20-\x7E\s]/g;
const extensions = [
  CleanPasteExtension.configure({
    regexPattern: customRegex, // customize the regex pattern used for cleaning pasted text
  }),
];

const TiptapEditor = () => {
  const editor = useEditor({
    extensions,
    content: "<p>Hello World!</p>",
  });
};
```
