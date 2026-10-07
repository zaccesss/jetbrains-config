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

## 5. Follow the system's light and dark setting

`colors/` holds two colour schemes that set only the console and terminal colours, on top of a
bundled editor scheme, so code keeps its usual highlighting:

| Scheme | Built on | Use with the theme |
| --- | --- | --- |
| High Contrast Dark | High contrast | High Contrast |
| High Contrast Light | Default (IntelliJ Light) | IntelliJ Light |

1. Settings > Editor > Color Scheme > gear icon > Import Scheme, once for each file in `colors/`.
2. Settings > Appearance & Behavior > Appearance: turn on **Sync with OS**, then use the gear icon
   beside it to pick High Contrast for dark and IntelliJ Light for light.
3. Switch the system to dark, pick High Contrast Dark under Editor > Color Scheme. Switch to light,
   pick High Contrast Light. The IDE remembers the scheme for each theme from then on.

The colours match the High Contrast palette in
[terminal-config](https://github.com/zaccesss/terminal-config), so a command's output reads the
same in the IDE's terminal as in any other terminal.

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

Copy the keymap into that directory's `keymaps/` folder, the file template into
`fileTemplates/internal/` and the colour schemes into `colors/`, then select the keymap in
Settings > Keymap. The system sync for step 5 goes in `options/laf.xml`:

```xml
<application>
  <component name="LafManager" autodetect="true">
    <laf themeId="JetBrainsHighContrastTheme" />
    <preferred-light-laf themeId="ExperimentalLight" />
    <preferred-dark-laf themeId="JetBrainsHighContrastTheme" />
    <lafs-to-previous-schemes>
      <laf-to-scheme laf="JetBrainsHighContrastTheme" scheme="High Contrast Dark" />
      <laf-to-scheme laf="ExperimentalLight" scheme="High Contrast Light" />
    </lafs-to-previous-schemes>
  </component>
</application>
```

## Adding another IDE

1. Build its plugin list from the installed plugins. For each plugin, read the real id and version
   from `META-INF/plugin.xml` inside its jar rather than guessing.
2. Save it as `plugins/<ide>.txt`, grouped under `//` category headers.
3. Add it to [plugins.md](plugins.md).
