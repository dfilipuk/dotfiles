# dotfiles

dotfiles and tooling for a portable development environment.

## Keyboard shortcuts

### fzf

Shortcut | Description
---------|------------
`Opt + C` | `cd` into the selected directory
`Ctrl + R` | Paste the selected command from history onto the command-line
`Ctrl + T` | Paste the selected files and directories onto the command-line
`Shift + Right` | Toggle preview
`Shift + Up` | Preview up
`Shift + Down` | Preview down
`Ctrl + F` | Preview page forward (down)
`Ctrl + B` | Preview page backward (up)
`Tab` / `Shift + Tab` | Select multiple files

### iTerm2

Shortcut | Description
---------|------------
`Cmd + N` | New window
`Cmd + T` | New tab
`Cmd + D` | Split vertically
`Cmd + Shift + D` | Split horizontally
`Cmd + W` | Close pane
`Cmd + Opt + W` | Close all panes in tab
`Cmd + Shift + W` | Close window

## Setup

### Git

#### Identity

- `git config [--global | --system] user.name "Name Surname"`
- `git config [--global | --system] user.email name.surname@example.com`

#### SSH key

Create `config` file in `~/.ssh` folder with content

```
Host host-alias
  HostName hostname
  User git
  IdentityFile path-to-private-key
  IdentitiesOnly yes
```

Use `host-alias` instead of hostname in URL, ex. `git clone git@host-alias:path-to-repo.git`

You want to include the option `IdentitiesOnly yes` to prevent the use of default ids. Otherwise, if you also have id files matching the default names, they will get tried first because unlike other config options (which abide by "first in wins") the `IdentityFile` option **appends** to the list of identities to try.

#### Config files

- system
  - Unix `/etc/gitconfig`
  - Windows `%ProgramFiles%\Git\mingw64\etc`
- global
  - `~/.gitconfig`
  - `~/.config/git/config`
- local
  - `[git-repositoy]/.git/config`

### iTerm2

- `Preferences` -> `General` -> `Settings`
    - `Load preferences from a custom folder or URL`
    - `Save changes` -> `Manually`

## Dependencies

[bat](https://github.com/sharkdp/bat) [fzf](https://github.com/junegunn/fzf) [ohmyzsh](https://github.com/ohmyzsh/ohmyzsh) [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions) [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)

## License

MIT License. See the [LICENSE](LICENSE) file for details.