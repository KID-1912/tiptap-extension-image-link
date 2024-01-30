# tiptap-extension-image-link

<h3 align="center">
    An extension that supports tiptap image link.
</h3>

<br/>

<p align="center">
  <a href="https://www.npmjs.com/package/tiptap-extension-image-link">
    <img
     alt="NPM URL"
     src="https://img.shields.io/badge/npm-tiptapExtensionImageLink?logo=npm">
  </a>
  <img
     alt="version"
     src="https://img.shields.io/badge/version-1.0.0-blue">
</p>

<br>

---

## Install

```shell
npm install tiptap-extension-image-link -S
```

## Usage

Insert an image link with the `setImageLink` command.

```js
editor
  .chain()
  .focus()
  .setImageLink({
    href: "This is the link url",
    src: "This is the image url",
    HTMLAttributes: {
      class: "image_link",
      "data-nickname": Name,
      "data-appid": AppID,
      "data-path": Path,
      "data-type": "image",
      "data-servicetype": "",
      target: "",
    },
  })
  .enter()
  .run();
```

## Options

You can configure common image link HTML attributes via the `HTMLAttributes` options

```js
import ImageLink from "tiptap-extension-image-link";

const editor = new Editor({
  element: document.querySelector(".editor"),
  extensions: [
    StarterKit,
    ImageLink.configure({
      HTMLAttributes: {
        class: "image-link",
      },
    }),
  ],
});
```

## Relations

**@tiptap/extension-link:** https://github.com/ueberdosis/tiptap/tree/develop/packages/extension-link

**tiptap-extension-link:** https://github.com/KID-1912/tiptap-extension-link

**tiptap-appmsg-editor:** https://github.com/KID-1912/tiptap-appmsg-editor
