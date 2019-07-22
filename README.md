# PRPL Demo APP

## Docs/slides

All docs & slides are availables at:

> **[fire.noelmace.com](http://fire.noelmace.com)**

## Light it up!

1. Install dependencies: `npm i`
1. Install nghttp2 (see instructions [below](#nghttp2))
1. Start: `npm start`
1. Test: open https://localhost:8443

### Requirements

#### nghttp2

In order to run the PRPL Demo App locally, you'll need the nghttpx command, which is part of the [nghttp2](https://nghttp2.org) library.

##### Mac OS X

1. install Homebrew:
   ```
   /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
   ```
1. run `brew install nghttp2`

##### Arch Linux

run `pacman -S nghttp2`

_details [here](https://www.archlinux.org/packages/extra/x86_64/nghttp2/)_

##### Windows

You'll need to build the package yourself. For detailed instructions, see the nghttp2 [documentation](https://nghttp2.org/documentation/package_README.html#notes-for-building-on-windows-msvc).

##### Other Linux distributions

You can edit package.json `prpl:start` to use [`./nghttpx`](./server/http2-proxy/nghttpx) instead of `nghttpx` if you use Linux.

Be aware that you may run into several issues doing so, as this is just a quick and dirty help. Please reach back to me if you do.

### Variations

You could also run some variations that you could find in `/steps`.

To do so, run:

1. `npm run api`
1. (in another terminal) `npm run step --step=<dirname>`

## :warning: Warning: May Contain Hot Topics

This project may contain a bunch of work in progress as I use it mainly to experiment new modern web capabilities and approach, in order to demonstrate them during my talks & workshops. As a result, there is a good chance that some part of it simply doesn't work, or that the documentation will not be sufficient by itself to allow a complete understanding. _This is especially the case with "steps" (`/steps` & `npm run step --step="step-name"`)._

**Please, open an issue if you have any question, request or suggestion!**
