+++ 
draft = true
date = 2023-10-16T17:01:35-04:00
title = "My Terminal Configuration Pt. 1: Neovim"
description = "My Neovim Setup"
slug = ""
authors = []
tags = []
categories = []
externalLink = ""
series = []
+++

### ...

[Coen Needel]() wrote a great piece piece last year on the history of Neovim, as well as on the underlying philosophy informing its design choices. A development environment that integrates with the terminal, is no fuss, .

The following is specific to my Debian environment...but [Coen's]() post has great explanations for where the following set up differs for other UNIX based OS's.

**Note** if you are new to neovim, I highly recommend going through the ~30 min tutorial by the Neovim team. In a neovim session, just run `:Tutor` to initiate.


### Configuring Neovim with Lua Script
- create directory for nvim config files: `~/.config/nvim`
- copy contents of `nvim_dots_minimal` to this directory
- upon running `nvim`, configurations will automatically be implemented


### Minimal Set Up
- my minimal lua configuration, [nvim_dots_minimal]()
    - core:
        - keymaps
        - plugins
        - options
    - config:
        - init.lua -> 
        - color scheme

For someone just trying to less painfully write scripts through an SSH connection, the above should be sufficient. What follows are additional plugins I'll append to the `config` section. This configuration is short enough that you can pretty easily study each component. Further, this setup should be easily **shareable**.

### Plugins: Adding Color Scheme, File Tree, Status Bar, and Helpful File Icons

Mercilessly borrowing (again) from [Coen](), I'll add the following set of plugins to my minimal set up.

First, update your `lua/core/plugins` file as follows. These additions will ensure that neovim has installed the necessary plugins prior to loading them.

```
return require('packer').startup(function(use)
    -- 1) Package Manager
  use 'wbthomason/packer.nvim'
    -- 2) Visuals
  use 'catppuccin/nvim'
    -- 3) File Tree, Helpful File Icons, 
  use { 'nvim-tree/nvim-tree.lua',
  requires = {
      'nvim-tree/nvim-web-devicons',
    }
  }
    -- 4) Status Bar
  use 'nvim-lualine/lualine.nvim'
  

-- ... -- More plugins can follow here


  -- Automatically set up your configuration after cloning packer.nvim
  -- Put this at the end after all plugins
  if packer_bootstrap then
      require('packer').sync()
    end
  end)
```

### Note: NerdFont

"In order for Nvim-Web-Devicons to work, you need to have a font installed that provides the unicode code points that it points to"


### Plugin Configuration

Next, update your `lua/config/` directory with a file for each plugin you wish to load. Also not the `init.lua` file, which invokes each plugin's corresopnding lua config file. Note that the `lua/config/init.lua` file is invoked in the `init.lua` file in the root directory. I borrowed my configuration settings and the idea to isolate plugin configurations in the `./lua/config` directory, again, from [Coen]().  


### Brief View Under the Hood and User Notes


**Packer:** Neovim Package Manager

**Nvim-Tree:** File Tree

**Lualine** Status Bar



https://dev.to/reobin/reload-init-vim-without-restarting-neovim-1h82
https://dev.to/iamdeb25/my-neovim-configuration-3ign
https://vonheikemen.github.io/devlog/tools/build-your-first-lua-config-for-neovim/
https://vonheikemen.github.io/devlog/tools/configuring-neovim-using-lua/
https://www.meetgor.com/neovim-vimscript-to-lua/
https://the-net-blog.netlify.app/post/configuring-neovim-with-lua-what-you-should-know/


https://medium.com/@shaikzahid0713/lualine-for-neovim-776b79861699
https://thevaluable.dev/tree-sitter-neovim-overview/




### Other vim learning resources
- *Learn Vim Progressively*:
  http://yannesposito.com/Scratch/en/blog/Learn-Vim-Progressively/
- *Learning Vim in 2013*:
  http://benmccormick.org/learning-vim-in-2014/
- *Vimcasts*:
  http://vimcasts.org/
- *Vim Video-Tutorials by Derek Wyatt*:
  http://derekwyatt.org/vim/tutorials/
- *Learn Vimscript the Hard Way*:
  http://learnvimscriptthehardway.stevelosh.com/
- *7 Habits of Effective Text Editing*:
  http://www.moolenaar.net/habits.html
- *vim-galore*:
  https://github.com/mhinz/vim-galore


### Appendix: Reminders For Myself 

Unfortunately, I sometimes forget commands. This happens everytime I spend more than a few weeks away from a development heavy pattern. I wrote [this]() appendix as a reference. One of the main complaints I've heard with respect to using terminal development environments, like neovim, is both the initial and subsequent learning curves. Tools like this should help.



