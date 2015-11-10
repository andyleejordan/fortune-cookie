# Fortune Cookie

This package prints a fortune in your scratch buffer, just like you
may have in your shell. If cowsay is installed, it can use that too.

## Usage

The minor mode will set `initial-scratch-message` with a fortune.

```elisp
(fortune-cookie-mode)
```

> If you don't use `package.el` you'll need to manually add the
> package to your load path and require it.

See the Emacs customize group `fortune-cookie` for the available
variables and their documentation (including command paths and flags).

The `fortune-cookie` interactive function can be called directly to
get a new fortune as a string.
