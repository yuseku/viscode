This repository contains my personal config for vscode inspired by neovim.

![Preview](preview.JPG)

## Keyboard shortcuts:
- `<leader>e` - Toggle sidebar with files
- `shift + l/h` - Switch tab left/right
- `ctrl + l/h` - Move tab left/right
- `<leader>gd` - Go to definition
- `<leader>vr` - Go to references
- `<leader>vh` - Hover
- `<leader>vc` - Open context menu
- `<leader>pf` - Search for files
- `<leader>pff` - Search for files with filters
- `<leader>ps` - Search for text
- `<leader>psf` - Search for text with filters
- `<leader>d` - Delete with void registry
- `<leader>p` - Paste with void registry
- `<leader>q` - Close buffer
- `<leader>up` - Upload local file to remote server
- `<leader>so` - Open workspace session

### Explorer:
- `r` - rename file
- `d` - remove file
- `c` - copy file
- `p` - paste file
- `y` - copy relative file path  

## Extensions:
- [`Vim`](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim)
- [`Catppuccin` (Theme)](https://marketplace.visualstudio.com/items?itemName=Catppuccin.catppuccin-vsc)
- [`FintItFaster` (Better search tool)](https://marketplace.visualstudio.com/items?itemName=TomRijndorp.find-it-faster)
    - Requirements:
        - [`fzf` (Command-line fuzzy finder)](https://github.com/junegunn/fzf)
        - [`rg` (Ripgrep)](https://github.com/BurntSushi/ripgrep)
        - [`bat` (A cat clone with wings)](https://github.com/sharkdp/bat)
- [`GlassIt` (Provides a transparent background)](https://marketplace.visualstudio.com/items?itemName=s-nlf-fh.glassit)
- [`NERDTree` (Basic functions to manage files explorer)](https://marketplace.visualstudio.com/items?itemName=Llam4u.nerdtree)
- [`JetBrains Icon Theme`](https://marketplace.visualstudio.com/items?itemName=chadalen.vscode-jetbrains-icon-theme)
- [`Sessions` (Create and switch workspaces with a keystroke)](https://marketplace.visualstudio.com/items?itemName=oigene.sessions)
- [`ftp-sync` (Synchronization of the local workspace (project files) with the server)](https://marketplace.visualstudio.com/items?itemName=lukasz-wronski.ftp-sync)
    - [Fix for `uploadOnSave` option](https://github.com/lukasz-wronski/vscode-ftp-sync/issues/307)

### `ftp-sync` configuration

Config:
```bash
{
    "remotePath": "/home/user/project/",
    "host": "000.00.00.000",
    "username": "user",
    "port": 00000,
    "protocol": "sftp",
    "uploadOnSave": false,
    "passive": true,
    "debug": false,
    "privateKeyPath": "/home/user/.ssh/id_rsa_dev",
    "ignore": [
        "\\.vscode",
        "\\.git"
    ]
}

```

Generated key must be in PEM:
```bash
ssh-keygen -f ~/.ssh/id_rsa_custom -m PEM -t rsa -C "user"
```

In addition, on windows, the `privateKeyPath` must have double backslashes, for example:
```bash
"privateKeyPath": "C:\\Users\\Administrator\\.ssh\\id_rsa_custom" 
```