# im-switch.nvim

Switch IMEs automatically based on vim modes. Written in pure lua only.
Currently, this plugin supports auto IME switch in markdown files and regular code comments.

## Installation

Dependencies: `fcitx5`, the plugin currently works for Linux only.

`lazy.nvim`
```lua
  {
    "yangrq1018/im-switch.nvim",
    enabled = function()
      return utils.executable('fcitx5-remote')
    end,
    dependencies = {'nvim-treesitter/nvim-treesitter'},
    opts = {},
  },
```

If you just want the functionality in markdown files, where people usually type a lot of
Chinese, you can lazy load the plugin by adding `ft = {'markdown'}`.

> Code is mainly modified from https://github.com/Kicamon/nvim
