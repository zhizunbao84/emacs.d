# A usable emacs config

This is my emacs configuration tree which originates from [that of Purcell's](https://github.com/purcell/emacs.d). But I eliminated many functions of that.

## Requirements
These are requirements that **must** be met:

* Emacs 24.4.1 or greater
* git 1.9.4 or greater


### Enable TLS for securely connecting to ELPA
ELPA is accessed over HTTP by default, which may result in security problems, so I prefer to use HTTPS instead. This can be done simply by replace the "http" in ELPA repository addresses with "https", and turn on the TLS checking.

By default, both HTTPS and TLS checking are **disabled**. If you do like to turn them on (and I recommend you to), then the following requirements must be met:

* remove the comment before `(require 'init-security)` line in `init.el`
* gnutls 3.4 or greater
* The `certifi` package from pypi (`pip install certifi`)


## Installation
To install, clone this repo to `~/.emacs.d`, i.e. ensure that the
`init.el` contained in this repo ends up at `~/.emacs.d/init.el`:

```
git clone https://github.com/xyguo/emacs.d.git ~/.emacs.d
```

Upon starting up Emacs for the first time, further third-party
packages will be automatically downloaded and installed.

## Update

Update the config with `git pull`. You'll probably also want/need to update
the third-party packages regularly too:

<kbd>M-x package-list-packages</kbd>, then <kbd>U</kbd> followed by <kbd>x</kbd>.




