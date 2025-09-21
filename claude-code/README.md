# Claude Code Setup Guide

## Installation

```sh
nvm install 22
nvm use 22
```

```sh
npm install -g @anthropic-ai/claude-code
```

## Remove old version

```sh
rm -rf ~/.nvm/versions/node/v22.18.0/lib/node_modules/@anthropic-ai/claude-code
rm -rf ~/.nvm/versions/node/v22.18.0/lib/node_modules/@anthropic-ai/.claude-code-*
```

## Configuring Claude Code For Kimi K2

This repo is a comprehensive guide on how to configure Claude Code for Kimi K2: <https://github.com/LLM-Red-Team/kimi-cc>

### Kimi Setup

- MacOS

TODO: correct this

```sh
vim ~/.zshrc
add two exports
```

- Windows

```sh
setx ANTHROPIC_BASE_URL "https://api.moonshot.cn/anthropic"
setx ANTHROPIC_AUTH_TOKEN ""
```

## Terminal Setup

Open claude code, use this command to setup terminal to allow for shift-enter to insert a new line in terminal.

```sh
/terminal-setup
```
