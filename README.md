# HyperTerm Visor

[![Join the chat at https://gitter.im/CWSpear/hyperterm-visor](https://badges.gitter.im/CWSpear/hyperterm-visor.svg)](https://gitter.im/CWSpear/hyperterm-visor?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Open your [HyperTerm](https://hyperterm.org/) terminal from anywhere with a global hotkey.

![HyperTerm Visor](https://cloud.githubusercontent.com/assets/495855/16907220/809ea6d0-4c76-11e6-956c-3329a0afc475.gif)

## Installation

In your `~/.hyperterm.js`, add `hyperterm-visor` to the list of `plugins`.

## Config

In your `~/.hyperterm.js`, you can define your hotkey (required) and the position (optional) you want your visor to be. It automatically will open on the screen where your mouse is.

```js
modules.exports = {
  config: {
    // other config...
    visor: {
      hotkey: 'CommandOrControl+Shift+Z',
      position: 'top', // or left, right, bottom
    },
  },
  // ...
};
```

You can define hotkeys as specified in the [Electron Accelerator docs](https://github.com/electron/electron/blob/master/docs/api/accelerator.md).

## Roadmap

* Better customization of where you can make the terminal appear.
* Option to always open on a specific monitor, etc.
* Double press mod keys to activate (i.e. hit Ctrl twice to activate).
* Create window if all windows have been closed.

## Caveats

* It always uses the most recently open window as your visor window.
* If all windows have been closed, it won't do anything until you manually open a new window.

This is pretty basic in its current form, and I'm labeling it as a beta as I use it and patch up edge cases, etc. I will build out more functionality and beef up this README as we go. 
