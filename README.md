gv.vim
======

A git commit browser.

![gv](https://cloud.githubusercontent.com/assets/700826/12355378/8bbf0834-bbdf-11e5-9389-1aba7cd1fec1.png)

[gitv](https://github.com/gregsexton/gitv) is nice. But I needed a faster, and
possibly simpler alternative that I can use with a project with thousands of
commits.

Installation
------------

Requires fugitive.

Using [vim-plug](https://github.com/junegunn/vim-plug):

```vim
Plug 'tpope/vim-fugitive'
Plug 'junegunn/gv.vim'
```

Usage
-----

### Commands

- `:GV` to open commit browser
    - You can pass `git log` options to the command, e.g. `:GV -S foobar`.
- `:GV!` will only list commits that affected the current file
- `:GV?` fills the location list with the revisions of the current file

`:GV` or `:GV?` can be used in visual mode to track the changes in the
selected lines.

### Mappings

- `o` or `<Space>` on a commit to display its content, `<CR>` to also
  switch window focus
- `o` or `<Space>` on commits to display the diff in the range, `<CR>` to
  also switch window focus
- `gb` for `:Gbrowse`
- `]]` and `[[` (or `J` and `K`) to move between commits
- `.` to start command-line with `:Git [CURSOR] SHA` à la fugitive
- `q` to close

Customization
-------------

`¯\_(ツ)_/¯`
