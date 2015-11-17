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

### Example

I use the following setup in my [.emacs.d][], which utilizes John
Wiegley's [use-package][]. It sets the `cowfile` to our favorite
mascot, Tux.

[.emacs.d]: https://github.com/andschwa/.emacs.d
[use-package]: https://github.com/jwiegley/use-package

```elisp
;; inhibit startup message
(setq inhibit-startup-message t)

(use-package fortune-cookie
  :config
  (setq fortune-cookie-cowsay-args  "-f tux -s")
  (fortune-cookie-mode))
```

Which placed this in my `*scratch*` buffer:

```elisp
;;  ___________________________________
;; / Pohl's law:                       \
;; |                                   |
;; | Nothing is so good that somebody, |
;; \ somewhere, will not hate it.      /
;;  -----------------------------------
;;    \
;;     \
;;         .--.
;;        |o_o |
;;        |:_/ |
;;       //   \ \
;;      (|     | )
;;     /'\_   _/`\
;;     \___)=(___/
```
