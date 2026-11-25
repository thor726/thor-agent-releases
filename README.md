# thor-agent-releases

Release distribution host for Thor Agent, served via GitHub Pages at
https://thor726.github.io/thor-agent-releases

This repository holds only published release artifacts and metadata:

- `releases/channels/` — release channel records (for example `stable.json`)
- `releases/termux/<channel>/` — the signed Termux APT repository
  (`dists/<suite>/`, `pool/`, `key.asc`)

Desktop installers are published as GitHub Release attachments on the main
Thor-agent repository, not as files in this repository.

## Status

Bootstrap (Fase 1 of the R2 to GitHub migration): hosting and layout only.
No Termux package has been published here yet, and the APT metadata in this
bootstrap is unsigned. Signed `InRelease` / `Release.gpg` and the matching
`key.asc` are produced by the Thor-agent release workflow when it stages a
real `.deb` with the `TERMUX_APT_GPG_KEY` secret. Do not install from this
bootstrap layout.

Source and release automation: https://github.com/thor726/Thor-agent
