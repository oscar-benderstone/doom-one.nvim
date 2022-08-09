<div align="center">

# doom-one.nvim

![License](https://img.shields.io/github/license/NTBBloodbath/doom-one.nvim?style=flat-square)
![Neovim version](https://img.shields.io/badge/Neovim-0.5-57A143?style=flat-square&logo=neovim)

[Features](#features) • [Install](#install) • [Screenshots](#screenshots) • [Contribute](#contribute)

</div>

> Come join the dark side, we have cookies.

This colorscheme is ported from [doom-emacs' doom-one].

## Notices
- `2022-08-08`: doom-one is now using Neovim global variables for configurations again.
  It is using the same configuration options, see [Install](#install).
- `2021-10-05`: doom-one configurations are now defined in a `setup` function,
  see [Install](#install) to know the valid setup options.
- `2021-06-16`: since the colorscheme is now 100% lua, your neovim must include
  [this](https://github.com/neovim/neovim/pull/14686).

## Features

- Optional terminal colors
- Optional italic comments
- Optional TreeSitter support
- Optional transparent background
- Optional support for numerous plugins (nvim-tree, barbar, lspsaga, etc)

## Install

Packer
```lua
use({
    'NTBBloodbath/doom-one.nvim',
    setup = function()
        -- Add color to cursor
		vim.g.doom_one_cursor_coloring = false
		-- Set :terminal colors
		vim.g.doom_one_terminal_colors = true
		-- Enable italic comments
		vim.g.doom_one_italic_comments = false
		-- Enable TS support
		vim.g.doom_one_enable_treesitter = true
		-- Color whole diagnostic text or only underline
        vim.g.doom_one_diagnostics_text_color = false
		-- Enable transparent background
		vim.g.doom_one_transparent_background = false

        -- Pumblend transparency
		vim.g.doom_one_pumblend_enable = false
		vim.g.doom_one_pumblend_transparency = 20

        -- Plugins integration
		vim.g.doom_one_plugin_neorg = true
		vim.g.doom_one_plugin_barbar = false
		vim.g.doom_one_plugin_telescope = false
		vim.g.doom_one_plugin_neogit = true
		vim.g.doom_one_plugin_nvim_tree = true
		vim.g.doom_one_plugin_dashboard = true
		vim.g.doom_one_plugin_startify = true
		vim.g.doom_one_plugin_whichkey = true
		vim.g.doom_one_plugin_indent_blankline = true
		vim.g.doom_one_plugin_vim_illuminate = true
		vim.g.doom_one_plugin_lspsaga = false
	end,
	config = function()
        vim.cmd("colorscheme doom-one")
    end,
})
```

> **IMPORTANT:** this colorscheme requires Neovim >= 0.6 to work.

## Extras

Extra color configs for [kitty] can be found in [extras](extras/). To use them,
refer to their respective documentation.

## Screenshots

> Dark variant:

![doom-one](./assets/doom-one.png)

> Light variant:

![doom-one-light](./assets/doom-one-light.png)

## Contribute

1. Fork it (https://github.com/NTBBloodbath/doom-one.nvim/fork)
2. Create your feature branch (<kbd>git checkout -b my-new-feature</kbd>)
3. Commit your changes (<kbd>git commit -am 'Add some feature'</kbd>)
4. Push to the branch (<kbd>git push origin my-new-feature</kbd>)
5. Create a new Pull Request

## License

`doom-one.nvim` is [MIT licensed](./LICENSE).

[doom-emacs' doom-one]: https://github.com/hlissner/emacs-doom-themes/blob/master/themes/doom-one-theme.el
[kitty]: https://github.com/kovidgoyal/kitty
