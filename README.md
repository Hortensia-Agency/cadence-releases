# Cadence releases

Public download page and installers for Cadence, which converts PRONOTE exports to SOPRA CSV files for HRA.
The app's source is private in `Hortensia-Agency/flet`; this repo only holds what buyers download.

- Page: `index.html`, served as a static site at https://cadence.hortensia-agency.com
- Installers: attached to this repo's GitHub Releases. The page links to
  `releases/latest/download/<file>`, so publishing a new release updates it with no page edit.

## Publishing a version

Build in the `flet` repo, then attach the files to a new release here. Keep these exact names, the page looks for them:

| File | Built with |
|---|---|
| `Cadence-windows.zip` | `dist\Cadence` from `pyinstaller PronoteCsvWatcher.spec`, zipped |
| `Cadence.dmg` | `./build_mac.sh` on a Mac |

```bash
gh release create v1.1.0 Cadence-windows.zip Cadence.dmg -R Hortensia-Agency/cadence-releases --title "Cadence 1.1.0"
```

Upload every platform to the same release: the page reads the latest release only, and shows
"macOS coming soon" when it has no `Cadence.dmg`.

## Screenshots

`screenshot-{fr,en}-{light,dark}.png` show fictional teachers only. Never replace them with captures of real school data.
