# SaveProof Core and CLI

Portable SaveProof verification core and an offline command-line client built
on its public API.

**Status: Repository bootstrap. Source migration and release publication are
pending.**

## Planned structure

```text
packages/core/   Portable verification library: @saveproof/core
apps/cli/        Offline CLI using the public core API
```

The core remains platform-independent. The CLI owns Node.js file access,
Workers, local storage and output. The core does not depend on the CLI.

This repository is intended to become the source of truth for both components
after their implementation, build tooling and tests are migrated here.
Website, server, database and production operations are outside its scope.

## Releases

Core and CLI have independent versions and release tags:

- `core-vX.Y.Z` for the standalone core package.
- `cli-vX.Y.Z` for the CLI, recording its exact bundled core version.

Release assets will include the accepted package, manifest and SHA256 checksums.
Official public delivery uses versioned HTTPS downloads on
[saveproof.org](https://saveproof.org); GitHub assets will mirror the same
verified bytes.

Until source migration, a tag in this repository will identify its release
record. Artifact manifests must separately identify the actual source revision
used to build the package. A repository snapshot is not a release package.

No implementation sources, release artifacts or tags are included in this
initial repository setup.
