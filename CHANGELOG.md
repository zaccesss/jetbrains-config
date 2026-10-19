# Changelog

All notable changes to this project are recorded here.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
Versioning follows [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [Unreleased]

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
