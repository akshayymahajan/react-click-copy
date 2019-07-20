# react-copy-content

> A Fully Customizable Click-To-Copy Component for React

[![NPM](https://img.shields.io/npm/v/react-copy-content.svg)](https://www.npmjs.com/package/react-copy-content) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Demo
![Demo](https://raw.githubusercontent.com/akshayymahajan/react-copy-content/master/demo.gif)

## Install

```bash
npm install --save react-copy-content
```

## Usage

```jsx
import ClickToCopy from 'react-copy-content'

<ClickToCopy contentToCopy="This will be copied to your clipboard." />
```

## Props
`contentToCopy: String`

This is the text that will be copied. It is a required prop.


`onCopy: function`
```jsx
<ClickToCopy
  contentToCopy="This will be copied to the clipboard"
  onCopy={() => console.log("copy")}
/>
```
This is the callback function triggered after the content is copied to the clipboard


`render: function`
```jsx
<ClickToCopy
  contentToCopy="This will be copied to the clipboard"
  render={props => (
    <a href="#copy" onClick={props.copy}>
      Copy
    </a>
  )}
/>
```
To render a custom component in place of the button, use the `render` prop. Inside your custom component, use `props.copy` to trigger the copy action.

## License

MIT © [akshayymahajan](https://github.com/akshayymahajan)
