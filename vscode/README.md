# VSCode Configuration Guide

## Extensions

- Generating extension list

```zsh
# macOS/Linux:
code --list-extensions | sort > .vscode/extensions.txt

# Windows (PowerShell):
code --list-extensions | Sort-Object > .vscode/extensions.txt
```

- Reinstall from list

```zsh
# macOS/Linux:
xargs -n1 code --install-extension < .vscode/extensions.txt
# Windows (PowerShell):
Get-Content .vscode/extensions.txt | ForEach-Object { code --install-extension $_ }
```

## Settings

- Get / Set settings:

Open command palette - Preferences: Open User Settings (JSON) - Choose from `Copy` or `Paste`
