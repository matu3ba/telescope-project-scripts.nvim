# telescope-project-scripts.nvim

An extension for [telescope-project.nvim](https://github.com/nvim-telescope/telescope-project.nvim)
that allows you to edit and run shell scripts associated to projects.

## Demo

TODO

## Setup

Add the following to your config:

```lua
require'telescope'.load_extension('project')
require'telescope'.load_extension('project-scripts')
```

You may skip explicitly loading extensions (they will then be lazy-loaded), but tab completions will not be available right away.

## Available functions:

### Edit shell scripts

Edit scripts:

```lua
require'telescope'.extensions.project-scripts.edit{}
```

## Default mappings (normal mode):

| Key | Description                                                   |
|-----|---------------------------------------------------------------|
| `d` | delete currently selected script                              |
| `r` | rename currently selected script                              |
| `c` | create a script\*                                             |
| `y` | copy script                                                   |
| `p` | paste script                                                  |
| `P` | Projects view                                                 |

## Default mappings (insert mode):

| Key | Description                                                   |
|-----|---------------------------------------------------------------|
| `<c-d>` | delete currently selected script                          |
| `<c-r>` | rename currently selected script                          |
| `<c-c>` | create a script\*                                         |
| `<c-y>` | copy script                                               |
| `<c-p>` | paste script                                              |
| `<c-P>` | Projects view                                             |

### Run shell scripts

Only the shell scripts inside the associated project folder are possible to run:

```lua
require'telescope'.extensions.project-scripts.run-script{}
```

**Non-Goals**

- placing scripts into custom paths
- backup and import of any sort
- restrict user on where the output of running scripts can be
- trying to abstract build systems or package management => use nix

**Roadmap :blue_car:**

- editing: document features :heavy_check_mark:
- changes: how should the plugin handle movement/deletion of projects? :construction:
- editing: document where things are stored :construction:
- editing: document file format :construction:
- editing: implementation :construction:
- running: document how this should work :construction:
- running: implement and document :construction:
- adjust to workspace addition of telescope-project.nvim ...
- link or document building (build systems and languages) :construction:
- link or document some shell stuff in neovim as goodies :construction:
