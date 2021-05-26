<h1 align="center">
One Pro
</h1>

![2021-May-26](https://user-images.githubusercontent.com/67771985/119711350-f873d780-be4e-11eb-8e87-25d5019ade9a.png)

![2021-May-26_1](https://user-images.githubusercontent.com/67771985/119711397-07f32080-be4f-11eb-9906-62b13af764d3.png)

## ✨ Features

- Customizable.
- Made to work with [treesitter](https://github.com/nvim-treesitter/nvim-treesitter).
- Support for built-in LSP.
- Support for some of the most popular plugins.
- Soft contrast for eye protection.
- Multiple options to enable italic and bold text.
- Vivid colors.

## Requirements

- [Neovim](https://github.com/neovim/neovim) >= 5.0

> NOTE: doesn't support [Vim](https://github.com/vim/vim), it uses lua.

## 📦 Installation

Use your favorite plugin manager. Example [packer](https://github.com/wbthomason/packer.nvim):

```lua
use "rafamadriz/onepro"
```

## 🚀 Usage

##### Neovim

To set the theme you can use the following.

```lua
vim.cmd[[colorscheme onepro]]
```

**To see all the available options do** `:help onepro-configuration` in Neovim

##### Lualine

To enable the [lualine](https://github.com/hoob3rt/lualine.nvim) theme, put this somewhere in your config:

```lua
require('lualine').setup {
  options = {
    -- ... your lualine config
    theme = 'onepro'
    -- ... your lualine config
  }
}
```

## ⚙️ Configuration:

> Note: the configuration options should be placed before `vim.cmd[[colorscheme onepro]]`

> To see all the options from neovim, you can execute `:help onepro.txt`

| Option                   | Default | Description                                                                                                                                           |
| ------------------------ | ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| `onepro_italic_comment`  | true    | Italic text for comments                                                                                                                              |
| `onepro_italic_keyword`  | false   | Applies to conditionals and keywords like `for`, `do`, `while`, `loops` etc.                                                                          |
| `onepro_italic_boolean ` | false   | `true` and `false`                                                                                                                                    |
| `onepro_italic_function` | false   | Applies to function (calls and definitions), method (calls and definitions) and built-in functions.                                                   |
| `onepro_italic_variable` | false   | Applies to variable names that are defined by the languages, like `this` or `self`. And any variable name that does not have another highlight group. |
| `onepro_bold`            | false   | Applies to error and warning messages, functions (calls and definitions), lsp virtual text, etc.                                                      |

#### Example config:

```lua
vim.g.onepro_italic_keyword = true
vim.g.onepro_italic_function = true

vim.cmd[[colorscheme onepro]]
```

## FAQ

It doesn't work as expected.

1. This color scheme is mainly designed for true colors, make sure of setting:
   `vim.o.termguicolors = true`

2. To test if your terminal supports true colors, use the following [script](https://gist.github.com/XVilka/8346728).

3. This colorscheme is made to look good with treesitter, if you don't have it, it won't look the same as the screenshoots.

### How to enable cursive italic keywords?

1. Install a font that supports italics, for example
   [JetBrains-NerdFont](https://www.nerdfonts.com/font-downloads) is an
   excellent font.

2. Set the correct italic font for your terminal of choice.

3. Enable italic text. E.g. `vim.g.onepro_italic_keyword = true`

### Supported plugins:

- [nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter)
- [nvim-tree](https://github.com/kyazdani42/nvim-tree.lua)
- [trouble.nvim](https://github.com/folke/trouble.nvim)
- [which-key.nvim](https://github.com/folke/which-key.nvim)
- [nvim-dap](https://github.com/mfussenegger/nvim-dap)
- [lspsaga.nvim](https://github.com/glepnir/lspsaga.nvim)
- [nvim-bufferline](https://github.com/akinsho/nvim-bufferline.lua)
- [neogit](https://github.com/TimUntersberger/neogit)
- [gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim)
- [vim-gitgutter](https://github.com/airblade/vim-gitgutter)
- [vim-signify](https://github.com/mhinz/vim-signify)
- [vim-syntastic](https://github.com/vim-syntastic/syntastic)
- [nerdtree](https://github.com/preservim/nerdtree)
- [ale](https://github.com/dense-analysis/ale)
- [vim-sneak](https://github.com/justinmk/vim-sneak)
- [indent-blankline](https://github.com/lukas-reineke/indent-blankline.nvim)
- [vim-startify](https://github.com/mhinz/vim-startify)
- [vim-easymotion](https://github.com/easymotion/vim-easymotion)
- [coc.nvim](https://github.com/neoclide/coc.nvim)

## TODO

- Add transparent option.
- Add support for terminals (kitty, alacritty, etc.)

## Acknowledgments

Inspired by [Doom One](https://github.com/hlissner/emacs-doom-themes) and [Edge](https://github.com/sainnhe/edge)
