# Setup

## 1. Install the IDEs

Install whichever JetBrains IDEs you use, through JetBrains Toolbox or the platform's supported
manual installation.

## 2. Install the plugins

For each IDE, install the plugins in its `plugins/<ide>.txt` through Settings > Plugins >
Marketplace, searching by plugin id (the part before the `@`).

> [!TIP]
> Each line pins the version that was installed at the time. Marketplace only offers versions
> compatible with your IDE build, so search by id and take the current version rather than hunting
> for the exact pinned one.

Install `com.intellij.plugins.vscodekeymap` before applying the custom keymap in step 4, since the
keymap's parent comes from that plugin.

## 3. Apply the Toolbox settings

Copy `toolbox/<platform>/settings.json` over Toolbox's own `settings.json` while Toolbox is not
running. Toolbox's default settings location differs per platform, see
[reference.md](reference.md#toolbox-settings).

## 4. Apply the keymap and file template

Use each IDE's own Settings UI:

- Keymap: Settings > Keymap > gear icon > Import Keymap, pick the file from `keymaps/` for your
  platform, then select it in the dropdown.
- File template: Settings > Editor > File and Code Templates > Files > Class, paste in the
  contents of `file-templates/Class.java`.

## Applying by file copy instead

Copying files straight into an IDE's config directory is safe only while that IDE is fully
closed. IntelliJ-family IDEs keep this state in memory while running and can overwrite an on-disk
file the moment a related setting changes.

Config directories are named per IDE and version, for example `IntelliJIdea2026.2` or
`PyCharm2026.2`:

| Platform | Config directory |
| --- | --- |
| macOS | `~/Library/Application Support/JetBrains/<IDE><version>` |
| Linux | `~/.config/JetBrains/<IDE><version>` |
| Windows | `%APPDATA%\JetBrains\<IDE><version>` |

Copy the keymap into that directory's `keymaps/` folder and the file template into
`fileTemplates/internal/`, then select the keymap in Settings > Keymap.

## Adding another IDE

1. Build its plugin list from the installed plugins. For each plugin, read the real id and version
   from `META-INF/plugin.xml` inside its jar rather than guessing.
2. Save it as `plugins/<ide>.txt`, grouped under `//` category headers.
3. Add it to [plugins.md](plugins.md).
