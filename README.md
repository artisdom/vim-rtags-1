vim-rtags
=========

C++ code navigation in Vim editor.

rtags uses clang to find symbol references, definitions, etc.


Setup
-----
Vundle can be used to install and update this plugin.

vim-rtags requires that Vim was compiled with `+byte_offset` enabled.

The rtags bin directory needs to be in your PATH.

Consider adding the following to your .vimrc:
```
nnoremap <silent> <localleader>r :call Rtags_references_to_symbol_under_cursor()<CR>
```

Recommended plugin: [Vim-unimpared](https://github.com/tpope/vim-unimpaired) which maps:
* `[l, ]l` to move up/down the lines in the "location list" window
* `[L, ]L` to move to first/last entry, and
* `[<C-L>, ]<C-L>` to jump to previous/next file.


To do
-----

* Make it work when a source file has not been saved. Note: buffers other than the current one may have significant unsaved changes. (A special case exists where a buffer has never been saved.) The simplest solution might be just to save everything that has been modified/created before calling rtags.
* Automatically start rdm. (rc should start rdm if it can't connect to rdm.)
* Lots more!
