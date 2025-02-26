# Neovim Configuration

This is my custom Neovim configuration. It includes various key mappings and settings for efficient navigation, testing, searching, and Git integration.

## Key Mappings

### Testing
- `<leader>t`: Run the nearest test (`:TestNearest`)
- `<leader>T`: Run the entire test file (`:TestFile`)
- `<leader>a`: Run the test suite (`:TestSuite`)
- `<leader>l`: Run the last test (`:TestLast`)
- `<leader>g`: Visit the test result (`:TestVisit`)

### File Navigation
- `<C-p>`: Open file finder (`builtin.find_files`)
- `<leader>fg`: Live grep search (`builtin.live_grep`)
- `<leader><leader>`: Show recently opened files (`builtin.oldfiles`)

### tmux Integration
- `<C-h>`: Navigate to the left pane in tmux (`NvimTmuxNavigateLeft`)
- `<C-j>`: Navigate to the bottom pane in tmux (`NvimTmuxNavigateDown`)
- `<C-k>`: Navigate to the top pane in tmux (`NvimTmuxNavigateUp`)
- `<C-l>`: Navigate to the right pane in tmux (`NvimTmuxNavigateRight`)

### LSP (Language Server Protocol)
- `K`: Show hover information (`vim.lsp.buf.hover`)
- `<leader>gd`: Go to definition (`vim.lsp.buf.definition`)
- `<leader>gr`: Find references (`vim.lsp.buf.references`)
- `<leader>ca`: Show code actions (`vim.lsp.buf.code_action`)
- `<leader>gf`: Format the current buffer using LSP (`vim.lsp.buf.format`)

### Git Integration
- `<leader>gp`: Preview the current Git hunk (`:Gitsigns preview_hunk`)
- `<leader>gt`: Toggle Git blame for the current line (`:Gitsigns toggle_current_line_blame`)

### Neotree (File Explorer)
- `<C-x>`: Open Neotree and reveal the file system (`:Neotree filesystem reveal left`)
- `<leader>bf`: Open Neotree and reveal the buffers (`:Neotree buffers reveal float`)

### Autocompletion (using `cmp`)
- `<C-b>`: Scroll documentation up (`cmp.mapping.scroll_docs(-4)`)
- `<C-f>`: Scroll documentation down (`cmp.mapping.scroll_docs(4)`)
- `<C-Space>`: Trigger completion (`cmp.mapping.complete()`)
- `<C-e>`: Abort completion (`cmp.mapping.abort()`)
- `<CR>`: Confirm selection in completion (`cmp.mapping.confirm({ select = true })`)

### Miscellaneous
- `<leader>h`: Clear search highlight (`:nohlsearch`)
- `:wincmd k`: Navigate to the top split
- `:wincmd j`: Navigate to the bottom split
- `:wincmd h`: Navigate to the left split
- `:wincmd l`: Navigate to the right split

## Settings

### Tabs and Indentation
- `expandtab`: Use spaces instead of tabs
- `tabstop=2`: Set the tab width to 2 spaces
- `softtabstop=2`: Set the soft tab stop to 2 spaces
- `shiftwidth=2`: Set the indent width to 2 spaces

### General
- `mapleader`: Set leader key to `Space`
- `background`: Set background to `light`
- `swapfile`: Disable swap files
- `number`: Show line numbers

### Test Strategy
- Set test strategy to `vimux` for integration with Vimux.

## Requirements

Make sure you have the following plugins installed to take full advantage of the key mappings and functionality:

- [vim-test](https://github.com/vim-test/vim-test)
- [telescope.nvim](https://github.com/nvim-telescope/telescope.nvim)
- [nvim-lspconfig](https://github.com/neovim/nvim-lspconfig)
- [gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim)
- [nvim-tmux-navigation](https://github.com/benmills/vimux)
- [cmp-nvim](https://github.com/hrsh7th/nvim-cmp)
- [neotree.nvim](https://github.com/nvim-neo-tree/neo-tree.nvim)

## Installation

LazyVim will automatically handle plugin installation and management for you. To get started with LazyVim, follow these steps:

1. Ensure that you have LazyVim installed. You can install LazyVim by following the instructions on the [LazyVim GitHub page](https://github.com/folke/lazy.nvim).

2. Install the plugins listed below by running:

```vim
:Lazy install
