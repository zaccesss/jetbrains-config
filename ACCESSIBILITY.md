# Accessibility

The keymap is built so one set of muscle memory covers JetBrains IDEs and VS Code.

> [!NOTE]
> Some of these settings are preferences rather than requirements. Change them freely in your own copy. If a change would help other people too, open an issue or a pull request so I can consider it for everyone.

## Keyboard

- The base keymap is the VS Code keymap (`VSCode OSX` on macOS, `VSCode` on Windows and Linux), so the standard editing, navigation and refactoring shortcuts match VS Code.
- Custom bindings use the same `Cmd+Alt` (macOS) or `Ctrl+Alt` (Windows and Linux) pair as [vscode-config](https://github.com/zaccesss/vscode-config). `Cmd+Alt+Q` runs a database console query in both editors.

> [!IMPORTANT]
> The base keymaps come from the `com.intellij.plugins.vscodekeymap` plugin. Install it before importing the custom keymap, otherwise the custom keymap has no parent and does not load. The order is in [guides/setup.md](guides/setup.md).

## Vision

- The IDE theme and editor colour scheme are Zacess Deep Contrast Dark from the Zacess Themes plugin: white on pure black with deep, fully saturated colours and yellow and cyan outlines. It stays fixed whatever the system appearance; **Sync with OS** switches to Zacess Deep Contrast Light in light mode. All eight Zacess themes come with the plugin.
- The console and terminal take their colours from the theme. The earlier High Contrast schemes in `colors/` stay available.
- Fonts live in each IDE's own settings, which this repository does not track. A screen reader option sits under Settings > Appearance & Behavior > Appearance.

## Feedback wanted

If something here gets in the way, open an [issue](https://github.com/zaccesss/jetbrains-config/issues/new/choose) describing what happened and what would work better.

## The shared statement

> [!NOTE]
> I keep one shared accessibility statement for all my projects: [zaccesss/accessibility](https://github.com/zaccesss/accessibility) or on [my site](https://isaacadjei.me/accessibility). This file takes precedence where the two differ.
