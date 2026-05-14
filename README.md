# homebrew-hookset

Homebrew tap for [hookset](https://github.com/bulga138/hookset) — a Git-native hook manager.

## Install

```bash
brew install bulga138/homebrew-hookset/hookset
```

Or:

```bash
brew tap bulga138/homebrew-hookset
brew install hookset
```

## What is hookset?

`hookset` uses Git 2.54's native `[hook]` configuration sections to define and run hooks. No Husky, no lint-staged, no committed scripts.

- **One binary** installed once per machine
- **One file** in your repo: `.hookset.toml`
- **No runtime dependencies** or package-manager hook runners

### Quick Start

```bash
# Install hookset
brew install bulga138/homebrew-hookset/hookset

# In your project
echo '[[hooks]]
name = "lint"
event = "pre-commit"
match = ["*.go"]
command = "go fmt ./..."' > .hookset.toml

hookset init
git commit -m "example"
```

## Upgrade

```bash
brew upgrade hookset
```

## Uninstall

```bash
brew uninstall hookset
brew untap bulga138/homebrew-hookset
```

## Requirements

- macOS, Linux, or Windows (with Git Bash)
- Git 2.54 or later

## Documentation

For full documentation, visit https://bulga138.github.io/hookset

## License

MIT
