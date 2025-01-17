---
title: Editor support
---

The editor of choice is still Emacs, but it is not the only one.

## Emacs

[SLIME](https://github.com/slime/slime/) is the Superior Lisp
Interaction Mode for Emacs. It has support for interacting with a
running Common Lisp process for compilation, debugging, documentation
lookup, cross-references, and so on. It works with many implementations.

[Portacle](https://shinmera.github.io/portacle/) is a portable and
multi-platform Common Lisp environment. It ships Emacs25, SBCL,
Quicklisp, SLIME and Git.

<img src="assets/portacle.png"
     style="width: 800px"/>

### Installing SLIME

SLIME is in the official GNU ELPA repository of Emacs Lisp packages
(in Emacs24 and forward). Install with:

    M-x package-install RET slime RET

Since SLIME is heavily modular and the defaults only do the bare minimum (not
even the SLIME REPL), you might want to enable more features with

~~~lisp
(slime-setup '(slime-fancy slime-quicklisp slime-asdf))
~~~

For more details, consult the
[documentation](https://common-lisp.net/project/slime/doc/html/) (also available
as an Info page).

Now you can run SLIME with `M-x slime` and/or `M-x slime-connect`.

See also:

* [https://wikemacs.org/wiki/SLIME](https://wikemacs.org/wiki/SLIME) - configuration examples and extensions.


### Using Emacs as an IDE

See ["Using Emacs as an IDE"](emacs-ide.html).


## Vim & Neovim

[Slimv](https://www.vim.org/scripts/script.php?script_id=2531) is a full-blown
environment for Common Lisp inside of Vim.

[Vlime](https://github.com/vlime/vlime) is a Common Lisp dev
environment for Vim (and Neovim), similar to SLIME for Emacs and SLIMV
for Vim.

<img src="assets/slimv.jpg"
     style="width: 800px"/>

[cl-neovim](https://github.com/adolenc/cl-neovim/) makes it possible to write
Neovim plugins in Common Lisp.

[quicklisp.nvim](https://gitlab.com/HiPhish/quicklisp.nvim) is a Neovim
frontend for Quicklisp.

[Slimv_box](https://github.com/justin2004/slimv_box) brings Vim, SBCL, ABCL,
and tmux in a Docker container for a quick installation.


## Eclipse

[Dandelion](https://github.com/Ragnaroek/dandelion) is a plugin for the
Eclipse IDE.

Available for Windows, Mac and Linux, built-in SBCL and CLISP support
and possibility to connect other environments, interactive debugger
with restarts, macro-expansion, parenthesis matching,…

<img src="dandelion.png" style="width: 800px"/>

## Lem

Lem is an editor tailored for Common Lisp development. Once you
install it, you can start developing. Its interface resembles Emacs
and SLIME (same shortcuts). It comes with an ncurses and an Electron
frontend, and other programming modes: Python, Go, Rust, JS, Nim,
Scheme, HTML, CSS, directory mode, a vim layer, and more.

<img src="assets/lem-terminal.png"
     style="width: 800px"/>

It can be started as a REPL right away in the terminal. Run it with:

    lem --eval "(lem-lisp-mode:start-lisp-repl t)"

So you probably want a shell alias:

    alias ilem='lem --eval "(lem-lisp-mode:start-lisp-repl t)"'

<img src="assets/lem1.png" style="width: 800px" title="Lem's REPL"/>


## Atom

See [SLIMA](https://github.com/neil-lindquist/slima). This package
allows you to interactively develop Common Lisp code, turning
Atom into a pretty good Lisp IDE.

<img src="assets/atom-slime.png"
     style="width: 800px"/>

## Sublime Text

[Sublime Text](http://www.sublimetext.com/3) has now good support for
Common Lisp.

First install the "SublimeREPL" package and then see the options
in Tools/SublimeREPL to choose your CL implementation.

Then [Slyblime](https://github.com/s-clerc/slyblime) ships IDE-like
features to interact with the running Lisp image. It is an
implementation of SLY and it uses the same backend (SLYNK). It
provides advanced features including a debugger with stack frame
inspection.

<img src="assets/editor-sublime.png"
     style="width: 800px"/>

## VSCode

[VSCode](https://code.visualstudio.com/) with [commonlisp-vscode extension](https://marketplace.visualstudio.com/items?itemName=ailisp.commonlisp-vscode)
supports running a REPL, evaluate code, auto indent, code completion, go to definition, documentation on hover, etc.
It's based on [cl-lsp](https://github.com/ailisp/cl-lsp) language server and it's possible to write LSP client that works in other editors.

<img src="assets/commonlisp-vscode.png" style="width: 800px"/>

## LispWorks (proprietary)

[LispWorks](http://www.lispworks.com/) is a Common Lisp implementation
that comes with its own Integrated Development Environment (IDE) and
its share of unique features, such as the CAPI GUI toolkit.  It is
**proprietary** and provides a **free limited version**.

You can [read our LispWorks review here](lispworks.html).

<img src="assets/lispworks/two-sided-view.png" style="width: 800px" title="The LispWorks listener an the editor in the Mate desktop environment"/>


## Geany (experimental)

[Geany-lisp](https://github.com/jasom/geany-lisp) is an experimental
lisp mode for the [Geany](https://geany.org/) editor. It features completion of symbols,
smart indenting, jump to definition, compilation of the current file and
highlighting of errors and warnings, a REPL, and a project skeleton creator.

<img src="assets/geany.png" style="width: 800px"/>


## Notebooks

[common-lisp-jupyter](https://github.com/yitzchak/common-lisp-jupyter) is a Common Lisp
kernel for Jupyter notebooks.

You can [see a live Jupyter notebook written in Lisp here](https://nbviewer.jupyter.org/github/yitzchak/common-lisp-jupyter/blob/master/examples/about.ipynb). It is easy to install (Roswell, repo2docker and Docker recipes).

<img src="assets/jupyterpreview.png"
     style="width: 800px"/>

There is also [Darkmatter](https://github.com/tamamu/darkmatter), a notebook-style
Common Lisp environment, built in Common Lisp.


## REPLs

[cl-repl](https://github.com/koji-kojiro/cl-repl) is an ipython-like REPL. It supports symbol completion, magic and shell commands, editing command in a file and a simple debugger.

You might also like [sbcli](https://github.com/hellerve/sbcli), an even simpler REPL with readline capabilities. It handles errors gracefully instead of showing a debugger.

<img src="assets/cl-repl.png"
     style="width: 500px"/>


## Others

There are some more editors out there, more or less discontinued, and
free versions of other Lisp vendors, such as Allegro CL.
