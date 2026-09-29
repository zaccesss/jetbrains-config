# Contributing

Thanks for taking an interest. Contributions are welcome: plugin list corrections, keymap
fixes and platform corrections.

## What belongs here

- A wrong plugin id or version in one of the `plugins/` lists
- A keymap binding that does nothing because its action id is wrong
- A Toolbox setting or default path that is wrong for a platform
- Improvements to the guides

## What does not belong here

- A plugin or binding that only reflects one person's preference rather than something broadly
  useful, keep that in your own copy

## How to contribute

1. Fork the repository and create a branch named `fix/<short-description>` or
   `feat/<short-description>`.
2. Make your change. For a plugin line, read the id and version from the plugin's own
   `META-INF/plugin.xml` rather than the folder name on disk. For a keymap binding, check the
   action id against the installed plugin's `plugin.xml` first.
3. Open a pull request with a clear title and a one-paragraph description of what changed and
   why. CI validates that every XML and JSON file parses and every plugin line is well formed.

## Style rules

> [!IMPORTANT]
> - **UK English** in prose and documentation.
> - **No secrets or licence keys**, ever.

## Reporting bugs

Open an issue with the IDE and version, your platform, what you expected versus what happened.

More about me and my work: [isaacadjei.me](https://isaacadjei.me).
