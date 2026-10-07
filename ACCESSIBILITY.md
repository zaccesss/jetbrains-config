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

- The IDE follows the system's light and dark setting: the built-in High Contrast theme in dark mode, IntelliJ Light in light mode.
- The two schemes in `colors/` give the console and terminal the High Contrast palette from [terminal-config](https://github.com/zaccesss/terminal-config): vivid colours on black in dark mode, every colour at 7:1 or more on white in light mode. Code highlighting stays the bundled scheme's own.
- Fonts live in each IDE's own settings, which this repository does not track. A screen reader option sits under Settings > Appearance & Behavior > Appearance.

## Feedback wanted

If something here gets in the way, open an [issue](https://github.com/zaccesss/jetbrains-config/issues/new/choose) describing what happened and what would work better.

## The shared statement

> [!NOTE]
> I keep one shared accessibility statement for all my projects: [zaccesss/accessibility](https://github.com/zaccesss/accessibility) or on [my site](https://isaacadjei.me/accessibility). This file takes precedence where the two differ.
