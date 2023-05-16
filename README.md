# ts-yamlpath.nvim

This is a little extension to nvim-treesitter's [statusline feature](https://github.com/nvim-treesitter/nvim-treesitter#statusline-indicator)
to print out your path in a yaml file.

## Usage

add the following to `ftplugin/yaml.lua`:

```lua
vim.keymap.set('n', '_', require('ts-yamlpath').path_at_cursor)
```

## Example

Consider the following yaml file:

```yaml
foo:
  bar:
    - "ok"
    - what: "fine"
```

With the cursor on "bar", the path will be `foo.bar`.
With the cursor on "fine", the path will be `foo.bar[1].what`

## Issues

I don't use this a _ton_, but I was fairly pleased with myself for getting it working.
If it doesn't do what you expect, please let me know.
