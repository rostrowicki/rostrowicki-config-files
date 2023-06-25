### PowerShell Setup (Windows)

[Chocolatey](https://docs.chocolatey.org/en-us/choco/setup) - Software Management for Windows
[LLVM](https://clang.llvm.org/) - Clang: a C language family frontend for LLVM
```bash
choco install llvm
```
[Nerd Fonts](https://www.nerdfonts.com/font-downloads) - Powerline-patched fonts. I use CascaydiaCove Mono.

[Scoop](https://scoop.sh/) - A command-line installer

[Git for Windows](https://gitforwindows.org/)

[Oh My Posh](https://ohmyposh.dev/) - Prompt theme engine [installation](https://ohmyposh.dev/docs/installation/prompt)

[Terminal Icons](https://github.com/devblackops/Terminal-Icons) - Folder and file icons

[Z](https://www.powershellgallery.com/packages/z) - directory jumper (*nix bash command equivalent)

[fzf](https://github.com/junegunn/fzf#installation) - fzf is a general-purpose command-line fuzzy finder. It's an interactive Unix filter for command-line that can be used with any list; files, command history, processes, hostnames, bookmarks, git commits, etc.
```> choco install fzf```

[PSFzf](https://github.com/kelleyma49/PSFzf) - PSFzf is a PowerShell module that wraps fzf, a fuzzy file finder for the command line.
```> scoop install psfzf```

#### Edit Powershell startup script to make it effective at PS startup
```bash
edit $PROFILE
```

```bash
# *profile.ps file:
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser # Optional: Needed to run a remote script the first time
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH/stelbent.minimal.omp.json" | Invoke-Expression
Import-Module -Name Terminal-Icons
```

### NeoVIM
After installing Neovim you should also install https://github.com/junegunn/vim-plug .

nvim config file on Windows should be placed in ~.\AppData\Local\nvim folder. If unsure then use following command :echo $MYVIMRC

Use :PlugInstall in nvim command mode to install plugins. To update run :PlugUpdate.

Note that there are several key bingings that are mapped in the config file.

