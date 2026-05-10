# JetBrains Air Theme for Zed

A dark Zed theme family inspired by JetBrains Air.

## Themes

- JetBrains Air Dark Blue
- JetBrains Air Dark Rosé
- JetBrains Air Dark Forest

## Local Development

Install this repository as a dev extension from Zed:

1. Open the command palette.
2. Run `zed: install dev extension`.
3. Select this repository.

The theme files live in `themes/` and use Zed's theme schema:
`https://zed.dev/schema/themes/v0.2.0.json`.

## Publishing

This repository is structured as a standalone Zed theme extension. Publish it by
adding it as a submodule to `zed-industries/extensions` under the
`extensions/jetbrains-air-theme` path and adding a matching `extensions.toml`
entry:

```toml
[jetbrains-air-theme]
submodule = "extensions/jetbrains-air-theme"
version = "0.0.1"
```

## License

MIT
