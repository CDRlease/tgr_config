# tgr_config

Public distribution repository for the formal release flow of
`JiepengTan/tg_config`.

This repository does not store source code. It stores mirrored GitHub Release
assets from the source repository, validates the release manifest plus bundle
checksums, and then notifies
`JiepengTan/tg_client`.

Current expected assets per tag:

- `config-bin-any-any.zip`
- `manifest.json`
- `SHA256SUMS.txt`

Current manifest contract for `config` releases:

- `mode` is `release`
- `component` is `config`
- the only `bundles[]` entry carries `name=config-bin-any-any.zip`
- the only `bundles[]` entry carries `os=any` and `arch=any`
- the only `bundles[]` entry carries a `bundle-entry-exists` validation with required `bin/` paths

Required secret:

- `CLIENT_DISPATCH_TOKEN`: token used to send `repository_dispatch` events to
  `JiepengTan/tg_client`
