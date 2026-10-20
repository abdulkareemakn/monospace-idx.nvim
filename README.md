# Monospace for Neovim

`monospace-idx.nvim` is a Neovim port of the Monospace themes for Visual Studio Code, with dark and light variants of the original Monospace, Space, and IDX Monospace themes.

## Variants

| Colorscheme | Variant | Source |
| --- | --- | --- |
| `monospace` | Monospace Dark | [monospace-theme](https://github.com/keksiqc/monospace-theme) |
| `monospace-light` | Monospace Light | [monospace-theme](https://github.com/keksiqc/monospace-theme) |
| `space` | Space Dark | [monospace-theme](https://github.com/keksiqc/monospace-theme) |
| `space-light` | Space Light | [monospace-theme](https://github.com/keksiqc/monospace-theme) |
| `idx-monospace` | IDX Monospace Dark | [idx-monospace](https://github.com/nnsng/idx-monospace) |
| `idx-monospace-light` | IDX Monospace Light | [idx-monospace](https://github.com/nnsng/idx-monospace) |
| `idx-monospace-flat` | IDX Monospace Dark Flat | [idx-monospace](https://github.com/nnsng/idx-monospace) |

The Monospace IDX Dark and Light themes from [monospace-idx-theme](https://github.com/amnweb/monospace-idx-theme) use the same palette and syntax colors as Monospace Dark and Light, so those two variants also cover that extension.

## Installation

### Neovim `vim.pack` (0.12+)

```lua
vim.pack.add({ "https://github.com/abdulkareemakn/monospace-idx.nvim" })
vim.cmd.colorscheme("monospace")
```

### [lazy.nvim](https://github.com/folke/lazy.nvim)

```lua
{
  "abdulkareemakn/monospace-idx.nvim",
  lazy = false,
  priority = 1000,
}
```

## Usage

Use `:colorscheme` with any of the variants above. Put the command in your `init.lua` to load it at startup:

```lua
vim.cmd.colorscheme("monospace")
```

The themes set terminal colors and support Neovim's built-in syntax, Tree-sitter, LSP and diagnostics. They also define highlights for Telescope, blink.cmp, nvim-cmp, Gitsigns, Neo-tree, nvim-tree, which-key, and Trouble. Those plugins are optional.

For [lualine.nvim](https://github.com/nvim-lualine/lualine.nvim), set `options.theme` to one of the colorscheme names:

```lua
require("lualine").setup({ options = { theme = "monospace" } })
```

The palettes are available at `require("monospace").palettes`. Keys containing hyphens need bracket notation:

```lua
local palettes = require("monospace").palettes
local dark = palettes.monospace
local light = palettes["monospace-light"]
```

## Development

The plugin follows Neovim's standard runtime layout: `colors/` provides the `:colorscheme` entry points, `lua/monospace.lua` holds palettes and highlights, and `lua/lualine/themes/` provides lualine themes.

## Credits

Palette and syntax intent come from these Visual Studio Code themes:

- [Monospace Theme](https://github.com/keksiqc/monospace-theme) by [Keksi](https://github.com/keksiqc)
- [IDX Monospace](https://github.com/nnsng/idx-monospace) by [nguyenngocsang](https://github.com/nnsng)
- [Monospace IDX Theme](https://github.com/amnweb/monospace-idx-theme) by [amnweb](https://github.com/amnweb)

## License

[MIT](LICENSE)
