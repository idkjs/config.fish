# config.fish

> 100% pure-<a href="https://fishshell.com" title="Portable Minimal Dotfiles ">fish</a> portable minimal dotfiles manager.

- fish implementation of [The best way to store your dotfiles: A bare Git repository](https://www.atlassian.com/git/tutorials/dotfiles) imagined by [StreakyCobra](https://news.ycombinator.com/item?id=11071754).

## Installation

[fisherman](https://github.com/jorgebucaran/fisher)(recommended)

```bash
fisher install idkjs/config
```

Run `git init --bare $HOME/.cfg`
Open a new terminal and run `config config --local status.showUntrackedFiles no`

## Manually

Run `make` or

```
cp functions/config.fish ~/.config/fish/functions/
```

Run `git init --bare $HOME/.cfg`
Open a new terminal and run `config config --local status.showUntrackedFiles no`


## Portability

If you need your config on a remote machine, just download your git repository and repeat the steps.

On new machine assuming you already have fish installed:

```bash
fisher install idkjs/config
echo ".cfg" >> .gitignore
git clone --bare <git-repo-url> $HOME/.cfg
```

Checkout the actual content from the bare repository to your $HOME:

```bash
config checkout
```

## Uninstalling

To uninstall run:

```bash
	rm -f $HOME/.config/fish/functions/config.fish

```
or
```
make uninstall
```

## License

[MIT](LICENSE.md)
