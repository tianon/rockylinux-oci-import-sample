# `rockylinux` `oci-import` sample

An example of using `oci-import` for `rockylinux`.

See:
- https://github.com/tianon/rockylinux-oci-import-sample/branches/all

An example `library/rockylinux`:

```yaml
Maintainers: ....
Builder: oci-import
File: index.json
# we have to have "generic" (not architecture-specific) values for these, but their exact values don't actually matter as long as they're valid
GitFetch: refs/heads/main
GitCommit: 483277cb0902c604c274889127c559446d422b1d

Tags: 9.6.20250531, 9.6, 9
Architectures: amd64, arm64v8
amd64-GitFetch: refs/heads/dist-9-amd64
amd64-GitCommit: 75a261c0ad9c7692d210ffb6b557f24167ad26cf
arm64v8-GitFetch: refs/heads/dist-9-arm64v8
arm64v8-GitCommit: 5e28456d55e7ea63707ebd1115a14e14fdff97af

Tags: 9.6.20250531-minimal, 9.6-minimal, 9-minimal
Architectures: amd64, arm64v8
amd64-GitFetch: refs/heads/dist-9-minimal-amd64
amd64-GitCommit: 359e51da84e3ad5faa8aec4850fa00899b39463f
arm64v8-GitFetch: refs/heads/dist-9-minimal-arm64v8
arm64v8-GitCommit: af1ebf205b2cb9c68f3e0bd91cf65e7db6589c34
```

(I only did two architectures of two variants of one version; hopefully that's enough to extrapolate to more architectures / versions 💚)
