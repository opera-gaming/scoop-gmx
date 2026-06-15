# opera-gaming/scoop-gmx

[Scoop](https://scoop.sh) bucket for the GameMaker eXperimental CLI (`gmx`) on Windows.

```powershell
scoop bucket add gmx https://github.com/opera-gaming/scoop-gmx
scoop install gmx
gmx --help
```

`gmx` ships as a prebuilt `x86_64` Windows binary — no Rust toolchain required.
Each release publishes the zip to this repo's
[releases](https://github.com/opera-gaming/scoop-gmx/releases) and updates `gmx.json`.

```powershell
scoop update gmx       # pull the newest release
scoop uninstall gmx
```

## Runtime

`gmx run` and `gmx debug` need a GameMaker runtime. The first time you use
either, gmx downloads the latest runtime into its cache and prints progress as
it goes. To do that explicitly up front:

```powershell
gmx runtime install
```

`gmx build`, `import`, `validate`, and `compile` work standalone.

## VS Code extension (.vsix)

The GameMakerX VS Code extension is published with each release (on the
Homebrew tap repo, which hosts the cross-platform assets):

```powershell
gh release download --repo opera-gaming/homebrew-gmx --pattern "gmx-vscode-*.vsix" --clobber
code --install-extension gmx-vscode-*.vsix
```

Or grab it from the
[releases page](https://github.com/opera-gaming/homebrew-gmx/releases) and run
`code --install-extension <file>.vsix`.

## See also

- [opera-gaming/gmx](https://github.com/opera-gaming/gmx) — source, issues, and docs (`gmx docs`)
- [opera-gaming/homebrew-gmx](https://github.com/opera-gaming/homebrew-gmx) — Homebrew tap (macOS / Linux)
