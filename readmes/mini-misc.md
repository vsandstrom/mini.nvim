<img src="https://github.com/echasnovski/media/blob/main/mini.nvim/logo/logo_misc.png" style="width: 100%"/>

<!-- badges: start -->
[![GitHub license](https://badgen.net/github/license/echasnovski/mini.nvim)](https://github.com/echasnovski/mini.nvim/blob/main/LICENSE)
<!-- [![GitHub tag](https://badgen.net/github/tag/echasnovski/mini.misc)](https://github.com/echasnovski/mini.misc/tags/) -->
<!-- [![Current version](https://badgen.net/badge/Current%20version/development/cyan)](https://github.com/echasnovski/mini.misc/blob/main/CHANGELOG.md) -->
<!-- badges: end -->

**Miscellaneous useful functions**

See more details in [help file](../doc/mini-misc.txt).

This is a part of [mini.nvim](https://github.com/echasnovski/mini.nvim) library. See its repository page to learn about common design principles and configuration recipes.

If you want to help this project grow but don't know where to start, check out [contributing guides](../CONTRIBUTING.md) or leave a Github star for 'mini.nvim' project.

## Demo

https://user-images.githubusercontent.com/24854248/173044891-69b0ccfd-3fe8-4639-bc70-f955bbf4a1a7.mp4

## Features

- `bench_time()` executes function several times and timing how long it took.
- `put()` and `put_text()` print Lua objects in command line and current buffer respectively.
- `stat_summary()` computes summary statistics of numerical array.
- `tbl_head()` and `tbl_tail()` return first and last elements of table.
- `zoom()` makes current buffer full screen in a floating window.

## Installation

<!-- This plugin can be installed as part of 'mini.nvim' library (**recommended**) or as a standalone Git repository. -->

There are two branches to install from:

- `main` (default, **recommended**) will have latest development version of plugin. All changes since last stable release should be perceived as being in beta testing phase (meaning they already passed alpha-testing and are moderately settled).
- `stable` will be updated only upon releases with code tested during public beta-testing phase in `main` branch.

Here are code snippets for some common installation methods (use only one):

- Using [wbthomason/packer.nvim](https://github.com/wbthomason/packer.nvim):

<table>
    <thead>
        <tr>
            <!-- <th>Github repo</th> -->
            <th>Branch</th> <th>Code snippet</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <!-- <td rowspan=2>'mini.nvim' library</td> -->
            <td>Main</td> <td><code>use 'echasnovski/mini.nvim'</code></td>
        </tr>
        <tr>
            <td>Stable</td> <td><code>use { 'echasnovski/mini.nvim', branch = 'stable' }</code></td>
        </tr>
        <!-- <tr> -->
        <!--     <td rowspan=2>Standalone plugin</td> <td>Main</td> <td><code>use 'echasnovski/mini.misc'</code></td> -->
        <!-- </tr> -->
        <!-- <tr> -->
        <!--     <td>Stable</td> <td><code>use { 'echasnovski/mini.misc', branch = 'stable' }</code></td> -->
        <!-- </tr> -->
    </tbody>
</table>

- Using [junegunn/vim-plug](https://github.com/junegunn/vim-plug):

<table>
    <thead>
        <tr>
            <!-- <th>Github repo</th> -->
            <th>Branch</th> <th>Code snippet</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <!-- <td rowspan=2>'mini.nvim' library</td> -->
            <td>Main</td> <td><code>Plug 'echasnovski/mini.nvim'</code></td>
        </tr>
        <tr>
            <td>Stable</td> <td><code>Plug 'echasnovski/mini.nvim', { 'branch': 'stable' }</code></td>
        </tr>
        <!-- <tr> -->
        <!--     <td rowspan=2>Standalone plugin</td> <td>Main</td> <td><code>Plug 'echasnovski/mini.misc'</code></td> -->
        <!-- </tr> -->
        <!-- <tr> -->
        <!--     <td>Stable</td> <td><code>Plug 'echasnovski/mini.misc', { 'branch': 'stable' }</code></td> -->
        <!-- </tr> -->
    </tbody>
</table>

**Important**: don't forget to call `require('mini.misc').setup()` to enable its functionality.

**Note**: if you are on Windows, there might be problems with too long file paths (like `error: unable to create file <some file name>: Filename too long`). Try doing one of the following:
- Enable corresponding git global config value: `git config --system core.longpaths true`. Then try to reinstall.
- Install plugin in other place with shorter path.

## Default config

```lua
-- No need to copy this inside `setup()`. Will be used automatically.
{
  -- Array of fields to make global (to be used as independent variables)
  make_global = { 'put', 'put_text' },
}
```

## Similar plugins

- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim)
