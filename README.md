# Simple Link Manager

This CLI tool allows to store & retrieve links with tags utilizing git repo storage.


## Install

[FZF](https://github.com/junegunn/fzf) should be installed to use this script. Try `brew install fzf` or `apt install fzf`.

Download shell script and place it somewhere in your `PATH`:
```bash
wget --no-cache --quiet "https://raw.githubusercontent.com/SmirnovAlexander/lnk/master/lnk" && chmod +x lnk && sudo mv lnk /usr/local/bin
```

Run `lnk init`

If you want to backup your local changes with remote repo:
1. Create new empty repo: https://github.com/new
2. `lnk git remote add origin remote-repo-url`
3. `lnk git push --set-upstream origin master`
4. When you want to push all chages to remote repo, run: `lnk git push`


## Usage

```
lnk init
    Initialize the link store.
lnk insert link-address
    Insert a new link.
lnk find [--no-browser,-n]
    Launches FZF to search for a link and open it in the browser.
    If --no-browser is specified, the link is just copied to the clipboard.
lnk git git-command-args...
    Execute a git command specified by git-command-args, e.g. 'lnk git push'
lnk update
    Update the script itself from source.
lnk help
    Show this text.
```
