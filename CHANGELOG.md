# Changelog

## 0.2.0+1.1.0

- **BREAKING**: `runc_checksum` isn't a static sha256 sum anymore. It's pointing to the `sha256sum` URL now of a specific release. So it doesn't needs to be adjusted anymore with every new release. The task just downloads the `runc.sha256sum` file and compares checksums.
- update `runc_version` to `1.1.0`
- add Molecule verification via `molecule verify -s kvm`
- add Molecule prepare step
- add `CHANGELOG.md`

## 0.1.0+1.0.2

- initial commit
