# jetbrains-config

> JetBrains IDE setup: plugin lists per IDE, a small custom keymap layered on the VS Code keymap
> and Toolbox settings for macOS, Linux and Windows.

JetBrains configuration is split by IDE (IntelliJ IDEA, PyCharm, WebStorm, CLion, DataSpell) as
well as by platform. This repo keeps the parts worth sharing in one place so every IDE points at
the same setup instead of drifting on its own defaults.

## What's here

- **`plugins/<ide>.txt`** - every non-bundled plugin installed in that IDE, one `plugin.id@version`
  per line, grouped under `//` category headers. Ids and versions come from each plugin's own
  `plugin.xml`, not the folder name JetBrains uses on disk. A plugin id and version are the same on
  every OS, so there is one list per IDE rather than one per platform. Every plugin is described in
  [guides/plugins.md](guides/plugins.md).
- **`keymaps/`** - a small custom keymap layered on top of the `VSCode OSX` and `VSCode` keymaps,
  one file for macOS and one for Windows and Linux. See [guides/reference.md](guides/reference.md#keymaps).
- **`file-templates/`** - a `Class.java` template with a `main` method.
- **`toolbox/<platform>/settings.json`** - JetBrains Toolbox's user-configurable settings.
  `shell_scripts.location` is the one value that differs per platform.

## Setup

Full walkthrough in [guides/setup.md](guides/setup.md).

> [!IMPORTANT]
> The custom keymaps use `VSCode OSX` or `VSCode` as their parent. Those keymaps come from the
> `com.intellij.plugins.vscodekeymap` plugin, so install it first or the custom keymap will not
> load.

## Structure

| Path | Contents |
| --- | --- |
| [`ACCESSIBILITY.md`](ACCESSIBILITY.md) | How the shared VS Code keymap keeps one set of shortcuts across editors |
| [`plugins/`](plugins/) | One plugin list per IDE |
| [`keymaps/`](keymaps/) | Custom keymaps for macOS and for Windows and Linux |
| [`file-templates/`](file-templates/) | The `Class.java` file template |
| [`toolbox/`](toolbox/) | JetBrains Toolbox settings, per platform |
| [`guides/`](guides/) | Setup walkthrough, settings reference and per-plugin detail |
