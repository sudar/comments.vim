comments.vim
=============

Global Plugin to comment and un-comment lines in different source files in both normal and visual <Shift-V> mode 

The following are the changes that I have done to the original Plugin

- Added support for Arduino files (both .pde and .ino)
- Added support for Pig files (.pig)
- Added support for Golang (.go) (by [Athom](https://github.com/athom))
- Added support for remapping the keys if needed
- Added support for Clojure and ClojureScript (by [seedano](https://github.com/ssedano/))
- Added support for Matlab and Octave (*.m) files

Credit goes to the original author Jasmeet Singh Anand.

Installation
============

Manual 
------
Stick this file in your ~/.vim/plugin directory or in some other 'plugin' directory that is in your runtime path

Using [Vundle](https://github.com/gmarik/vundle)
-------------

```VimL

    Bundle "sudar/comments.vim"

    And :BundleInstall

```

Configuration
=============

By default, the following keys are mapped

- Ctrl-c - to comment a single line or visual block
- Ctrl-x - to un-comment a single line or visual block

You can map your own keys if needed

```VimL


    let g:comments_map_keys = 0

    " key-mappings for comment line in normal mode
    noremap  <silent> <C-L> :call CommentLine()<CR>
    " key-mappings for range comment lines in visual <Shift-V> mode
    vnoremap <silent> <C-L> :call RangeCommentLine()<CR>

    " key-mappings for un-comment line in normal mode
    noremap  <silent> <C-K> :call UnCommentLine()<CR>
    " key-mappings for range un-comment lines in visual <Shift-V> mode
    vnoremap <silent> <C-K> :call RangeUnCommentLine()<CR>

```


Original Readme file
====================
This is a mirror of http://www.vim.org/scripts/script.php?script_id=1528

Global Plugin to comment and un-comment lines in different source files in both normal and visual <Shift-V> mode
usage:
ctrl-c to comment a single line
ctrl-x to un-comment a single line
shift-v and select multiple lines, then ctrl-c to comment the selected multiple lines
shift-v and select multiple lines, then ctrl-x to un-comment the selected multiple lines
supports: c, c++, java, php[2345], proc, css, html, htm, xml, xhtml, vim, vimrc, sql, sh, ksh, csh, perl, tex, fortran, ml, caml, ocaml, vhdl, haskel and normal files
