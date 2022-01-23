Vimwiki is a personal wiki for Vim – interlinked, plain text files written in a markup language

# With Vimwiki you can
 * organize notes and ideas and quickly create links between them
 * manage todo-lists
 * write a diary

## Features
* three markup syntaxes supported: Vimwiki's own syntax, Markdown, MediaWiki
* export everything to HTML
* link to other wiki pages and external files
* search through all wiki pages
* outline notes and tasks in indented lists
* quickly manipulate numbered and bulleted lists
* tag wiki pages or arbitrary places and quickly jump to tags
* auto-formatted tables

Screenshots
----------------

![screenshot1](https://raw.githubusercontent.com/vimwiki/vimwiki/master/doc/screenshot_1.png)
![screenshot2](https://raw.githubusercontent.com/vimwiki/vimwiki/master/doc/screenshot_2.png)

# Quickstart
Press `<Leader>ww` (this is usually `\ww`) to go to your index
page.  By default it is located in `~/vimwiki/index.wiki`.

Feed it with the following example:

    = My knowledge base =
        * Tasks -- things to be done _yesterday_!!!
        * Project Gutenberg -- good books are power.
        * Scratchpad -- various temporary stuff.

Place your cursor on `Tasks` and press Enter to create a link.  Press Enter again to
open it.  Edit the new page, save it, and press Backspace to jump back to your
index.

A Vimwiki link can be constructed from more than one word.  Just visually
select the words to be linked and press Enter.  Try it with `Project Gutenberg`.
The result should look something like:

    = My knowledge base =
        * [[Tasks]] -- things to be done _yesterday_!!!
        * [[Project Gutenberg]] -- good books are power.
        * Scratchpad -- various temporary stuff.

See `:h vimwiki` for the full documentation.

Basic markup (default syntax)
------------------------------------------------------------------------------

    = Header1 =
    == Header2 ==
    === Header3 ===

    *bold text*
    _italic text_

    [[wiki link]]
    [[wiki link|description]]

    * bullet list item 1
    * bullet list item 2
        a) numbered list item 1
        b) numbered list item 2

    {{{python
    def greet(s):
        print("Hello, " + s)
    }}}

    | a table |  |
    |---------|--|
    |         |  |

For other syntax elements, see `:h vimwiki-syntax`

Key bindings
------------------------------------------------------------------------------

 * `<Leader>ww` – Open the default wiki index file
 * `<Leader>ws` – Select and open wiki index file
 * `<Enter>` – Follow/Create wiki link
 * `<Backspace>` – Go back to parent(previous) wiki link
 * `<Tab>` – Find next wiki link
 * `<Shift-Tab>` – Find previous wiki link

For more keys, see `:h vimwiki-mappings`


Commands
------------------------------------------------------------------------------

 * `:Vimwiki2HTML` – Convert current wiki page to HTML
 * `:VimwikiAll2HTML` – Convert all your wiki pages to HTML
 
For more, see `:h vimwiki-commands`

Installation
==============================================================================

Prerequisites
------------------------------------------------------------------------------

Make sure you have these settings in your vimrc file:

    set nocompatible
    filetype plugin on
    syntax on

Without them Vimwiki will not work properly.


Installation using [Pathogen](http://www.vim.org/scripts/script.php?script_id=2332)
------------------------------------------------------------------------------

    cd ~/.vim
    mkdir bundle
    cd bundle
    git clone https://github.com/vimwiki/vimwiki.git

Alternatively, download the latest stable version ([zip](http://github.com/vimwiki/vimwiki/zipball/master) [tar](http://github.com/vimwiki/vimwiki/tarball/master)) or the latest development version ([zip](http://github.com/vimwiki/vimwiki/zipball/dev) [tar](http://github.com/vimwiki/vimwiki/tarball/dev)) and extract it into `~/.vim/bundle/`

Then launch Vim, run `:Helptags` and then `:help vimwiki` to verify it was installed.