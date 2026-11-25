# software_releases

Version files for illumiSonics desktop apps. Installed copies of **dataman** and **SlideReg** read
their file here to tell users when a newer version is available. The apps themselves are
downloaded from their private releases pages (approved users only).

| App | Version file | Downloads |
|---|---|---|
| dataman | [dataman.json](dataman.json) | [dataman_releases](https://github.com/illumiSonics/dataman_releases/releases/latest) |
| SlideReg | [slidereg.json](slidereg.json) | [slidereg_releases](https://github.com/illumiSonics/slidereg_releases/releases/latest) |

Each file is written by the app's release workflow when a version is published:

```json
{"version": "0.4.0", "published": "2026-12-01", "notes": "What's new, in one line",
 "download": "https://github.com/illumiSonics/dataman_releases/releases/tag/v0.4.0"}
```

To warn every user of an older version more strongly ("Please update"), add
`"min_version": "0.4.0"` to the file by hand. Later releases keep it.

The apps only download this file. They send nothing about the user, their computer or their data.
