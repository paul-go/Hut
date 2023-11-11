<p align="center">
	<img src="readme-poster.png" alt="RawJS Poster Image">
</p>

[![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=Is%20React%20too%20complicated%3F%20Give%20Raw.js%20a%20go.&url=https://github.com/scrollapp/rawjs)

## What is RawJS?

RawJS an **ultra-ergonomic HTML element construction library** that is designed to facilitate the construction of complex user interfaces with in a zero-magic, vanilla TypeScript style. Call functions. Create HTMLElement objects with event bindings and CSS styling attached. That's it.

It turns out, this is all you need to create complex interactive UIs. **You don't need React, Vue, Angular, Svelte**, or any of the others. These things are complicated UI sub-systems that run around behind the scenes and do a bunch of weird magic for you in order to keep your view in sync with your data. You have to do things their way, otherwise, the magic won't work.

Frameworks tend to do a lot of reinventing of what you can already do in JavaScript. By making controllers that are just plain TypeScript classes, and using the DOM directly to store your view state, you can cut complexities associated with model/view synchronization. Some devs will shudder at this. But this technique can **vastly** reduce total project complexity. Code gets easier to debug. WTF moments reduce in frequency. Total project risk goes down.

## RawJS Features:

- No learning curve (assuming you know JavaScript and how to work the DOM).
- No props / state / special controller classes that need to be inherited.
- No weird or unpredictable framework "magic".
- No bloat. The whole library is only **2.3KB**.
- No performance overhead.
- No virtual DOM.
- No JSX.
- **No external CSS / SASS / LESS** files needed. Write your CSS in TypeScript, and get all the benefits of styling becoming just another part of the code.
- **No more asking StackOverflow: "How do I do X in framework Y?"**. RawJS gives it to you raw. It's just you and the DOM. Do whatever makes sense.

Also:

- RawJS is being used in production (to build the Direct app).
- Many years in the making. Has passed through many different design variations.
- Works as a `<script>` include, as a module, or as a `require()`.
- Works in Node.js / Deno for server-side HTML generation.

## Reasons Not Use RawJS?

- **React / Vue / Svelte have stronger ecosystems**. But for a battle-tested 2.3KB library that's not doing very much, how important really is an ecosystem?
- No mobile-native UI (React Native) equivalent. If someone wants to make a RawJS backend for NativeScript, DM me on Twitter.

## Installation

```html
<script src="https://cdn.jsdelivr.net/npm/rawjs/raw.min.js"></script>
```
Or
```
npm install rawjs --save
```
Or
```html
<script type="module" src="https://cdn.jsdelivr.net/npm/rawjs/raw.esm.js"></script>
```

## Usage

For ES Modules usage:
```typescript
import * as raw from "rawjs";

document.body.append(
	raw.div(
		{
			padding: "100px",
			background: "red",
		},
		raw.on("click", () => alert("Hello world"))
	)
);
```

For global usage:
```typescript
const raw = new Raw();

document.body.append(
	raw.div(
		{
			padding: "100px",
			background: "red",
		},
		raw.on("click", () => alert("Hello world"))
	)
);
```

See more examples at the [quickstart](quickstart.md).
