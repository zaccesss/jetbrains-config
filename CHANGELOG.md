# Changelog

All notable changes to this project are recorded here.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
Versioning follows [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [Unreleased]

## [0.0.1] - 2026-10-22

### Added

- `options/terminal-font.xml` sets the built-in terminal to GeistMono Nerd Font, so Nerd Font prompt symbols draw. The font is free and must be installed from the Nerd Fonts releases; setup step 6 links it and covers the Settings route.

### Changed

- The theme is now Zacess Deep Contrast Dark from the Zacess Themes plugin (`com.zacess.themes@0.3.0`, added to every list in `plugins/`), fixed whatever the system appearance, in place of the built-in High Contrast theme following the system. `options/laf.xml` and `options/colors.scheme.xml` hold the setting with the Deep Contrast pair ready for Sync with OS. The earlier High Contrast schemes stay in `colors/`.

## 2026-10-19

### Added

- High Contrast Dark and High Contrast Light colour schemes in `colors/`, with setup steps for following the system's light and dark setting.
- Initial release: plugin lists for IntelliJ IDEA, PyCharm, WebStorm, CLion and DataSpell
- Custom keymaps for macOS and for Windows and Linux, layered on the VS Code base keymaps
- A `Class.java` file template
- JetBrains Toolbox settings for macOS, Linux and Windows
- Setup, reference and plugin guides
- CI that validates the XML, JSON and plugin list formats
- `ACCESSIBILITY.md`: how the shared VS Code keymap keeps one set of shortcuts across editors.

### Changed

- `ACCESSIBILITY.md`: a note that the settings are preferences, a callout for the keymap plugin that must be installed first and a link to the shared accessibility statement.
- Tidied code comments and the contributor guide.

### Fixed

- The setup and plugin guides now warn that `intellij.vitejs` from the DataSpell list does not install on DataSpell 2026.1, since Marketplace has no Vite build for it.
