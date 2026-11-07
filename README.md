# dotfiles

Run `./install.sh` to set up a new macos machine.

## Private local files (not in this repo)

On a new work laptop, create these two files by hand after installing:

`~/.gitconfig.local`
```ini
[user]
    email = YOUR_WORK_EMAIL
    name = YOUR_GITHUB_USERNAME
```

`~/.zshrc.local`
```zsh
export NPM_PRIVATE_REGISTRY="YOUR_PRIVATE_REGISTRY_URL"
```

Without the first, git commits fail (`useConfigOnly`). Without the second, `npmprivate` fails.

# verify
check if the registry env var actually got sourced by .zshrc, since it doesn't warn you if it failed and `npmprivate` won't work.
```
echo $NPM_PRIVATE_REGISTRY
```
