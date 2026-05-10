# JetBrains Air Theme for Zed

A dark Zed theme family inspired by the JetBrains Air IDE aesthetic.

## Included Themes

- `JetBrains Air Dark Blue`: the default JetBrains Air-inspired blue palette.
- `JetBrains Air Dark Rosé`: a warm rose and violet variant.
- `JetBrains Air Dark Forest`: a green, low-glare variant.

## Installation

### From Zed

After release, install the extension from Zed's extension store:

1. Open the command palette.
2. Run `zed: extensions`.
3. Search for `JetBrains Air`.
4. Install the extension and select one of the `JetBrains Air` themes from the theme selector.

### Local Development

Install this repository as a dev extension from Zed:

1. Open the command palette.
2. Run `zed: install dev extension`.
3. Select this repository.
4. Open the theme selector and choose one of the `JetBrains Air` themes.

## Repository Layout

- `extension.toml`: Zed extension manifest.
- `themes/jetbrains-air.json`: theme family definition using Zed's theme schema.
- `LICENSE`: MIT license.

The theme file targets Zed's theme schema:
`https://zed.dev/schema/themes/v0.2.0.json`.

## Validation

Before publishing, validate the theme JSON and extension manifest:

```sh
jq empty themes/jetbrains-air.json
python3 -m jsonschema -i themes/jetbrains-air.json /tmp/zed-theme-schema.json
python3 -c 'import tomllib, pathlib; tomllib.loads(pathlib.Path("extension.toml").read_text())'
```

To fetch the current Zed theme schema for local validation:

```sh
curl -fsSL https://zed.dev/schema/themes/v0.2.0.json -o /tmp/zed-theme-schema.json
```

## Publishing

This repository is structured as a standalone Zed theme extension. Publish it by
adding it as a submodule to `zed-industries/extensions` under the
`extensions/jetbrains-air` path and adding a matching `extensions.toml` entry.
The version in `zed-industries/extensions` must match the version in
`extension.toml`.

```toml
[jetbrains-air-theme]
submodule = "extensions/jetbrains-air"
version = "0.0.1"
```

Current manifest metadata:

- Extension id: `jetbrains-air`
- Extension name: `JetBrains Air`
- Version: `0.0.1`
- Repository: `https://github.com/ArjunKhunti/zed-jetbrains-air-theme`

## License

MIT
