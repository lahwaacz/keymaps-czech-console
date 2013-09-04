## keymaps-czech-console

Czech keyboard maps for Linux console

Since [kbd](http://www.kbd-project.org/) version 2.0.0 the frequently used Czech keymaps `cz.map` (both QWERTZ and QWERTY layouts) are completely broken.<sup>[[1]](https://bugs.archlinux.org/task/36689)[[2]](https://bbs.archlinux.org/viewtopic.php?id=168839)</sup>

Because searching for the source of this bug in one bulky commit<sup>[[3]](https://bbs.archlinux.org/viewtopic.php?pid=1319932#p1319932)</sup> is really annoying and the original `cz.map` is pretty complex and practically unfixable (90KB in file size is too much), the simplest solution turned out to be writing new keymap from scratch.

These keymaps are not direct replacement for the original `cz.map`, multiple features were dropped (like switching between `cz` and `us` layouts) and some keybindings are different (some special characters, compose mode). I take it as a great improvement over the original layout as it is, but it should be treated as an independent new keymap.

__Future contributions are welcome - I'm sure that I forgot to add some features.__

### Features

* Works with `kbd-2.0.0`.
* High usage of `include` statement, so common parts are used. As a consequence, the code is much simpler and easy to maintain.
* Special characters bound to the `AltGr` modifier, preferably it produces a character from `us` layout (if there is a difference from the `cz` layout).

### Dropped features (won't implement)

* Switching between multiple layouts (namely `cz` and `us`)
