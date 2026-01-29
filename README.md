# tree-sitter-oxi

A Treesitter parser for Oxi.

## Neovim Integration (nvim-treesitter)

To use this parser with Neovim locally for development:

```lua
local parser_config = require("nvim-treesitter.parsers").get_parser_configs()

parser_config.oxi = {
  install_info = {
    url = "https://github.com/oxilang/tree-sitter-oxi.git",
    files = { "src/parser.c" },
    branch = "main",
    generate_requires_npm = false,
    requires_generate_from_grammar = false,
  },
  filetype = "oxi",
}

vim.filetype.add({
  extension = {
    oxi = "oxi",
  },
})
```
