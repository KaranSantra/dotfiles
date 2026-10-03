# Project notes for agents

Deliberate decisions in this repo - do NOT silently revert them:

- This is Karan's fork of kunchenguid/dotfiles, deliberately diverged in four places - do NOT revert them when merging upstream:
  - `homebrew.onActivation.cleanup = "none"`: this Mac keeps Homebrew packages installed outside `configuration.nix` (firstmate depends on tmux and gh).
  - No `wezterm` or `claude-code` casks: both are installed outside Homebrew here.
  - `home.nix` does not link Claude settings, global agent instructions (`home/AGENTS.md`), or Pi configs: this Mac keeps its own.
  - `home.nix` zsh carries this Mac's own environment (nvm, pnpm, pyenv, Android, Docker, cargo) and `cc` keeps `--chrome`.
- Never commit `.no-mistakes/` validation evidence to this public repo. `.no-mistakes/` is gitignored; if a validation pipeline stages evidence into a branch, drop it before merging.

## Maintaining this file

Keep this file for knowledge useful to almost every future agent session in this project.
Do not repeat what the codebase already shows; point to the authoritative file or command instead.
Prefer rewriting or pruning existing entries over appending new ones.
When updating this file, preserve this bar for all agents and keep entries concise.
