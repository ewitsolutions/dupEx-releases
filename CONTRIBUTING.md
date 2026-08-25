# Contributing

This repository carries the released packages of dupEx and its issue tracker. The source code is not public, so **code contributions are not possible** — a pull request here has nothing to attach to. That is not a judgement of the offer; it is simply how the project is set up.

What genuinely helps:

## Bug reports

Open an issue with the bug report form. It asks for the version, the package format, the distribution and a log excerpt — those four turn most reports into something reproducible on the first read.

Where the log lives depends on the package format, because the Flatpak and the Snap remap `HOME`:

  * deb, rpm, tar.gz, AppImage — `~/.local/share/dupEx/logs`
  * Flatpak — `~/.var/app/com.ewitsolutions.dupEx/data/dupEx/logs`
  * Snap — `~/snap/dupex/current/.local/share/dupEx/logs`

The session log names its own location in the debug section at the top, so the surest way is to open the newest file and read the "Logs" line. It records the scan parameters and the detected storage medium, and it contains file paths, so remove anything you would rather not publish before pasting.

## Feature requests

Also an issue, with the feature request form. Worth writing down: what you were trying to do when the gap showed up. A described situation is easier to answer well than a described solution.

## Translation corrections

dupEx ships in 23 languages, and the non-English texts have not all been read by native speakers. If a menu entry or a message reads wrong in your language, an issue naming the language and the exact string is very welcome — including the context menu entry your file manager shows.

## Security problems

Not here. See [SECURITY.md](SECURITY.md) — those go to support@ewitsolutions.com so a fix can ship before details are public.
