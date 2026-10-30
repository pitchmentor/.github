# Contributing to Pitch Mentor

Thanks for helping improve the Pitch Mentor API clients. This guide applies to every repository in the
[pitchmentor](https://github.com/pitchmentor) organization unless a repository has its own `CONTRIBUTING.md`.

## Before you start

- **Questions** belong on [Discord](https://discord.gg/SkcxVEJ6wQ); issues are for bugs and concrete proposals.
- **Security problems** must not be reported in public issues. See [SECURITY.md](SECURITY.md).
- **Bigger changes** (new public APIs, behavior changes): open an issue first so we can agree on the approach.

## Generated code

The SDKs (`pitchmentor-node`, `pitchmentor-python`, `pitchmentor-go`) are generated from the live OpenAPI spec at
`https://api.pitchmentor.net/v1/openapi.json`. Files marked `DO NOT EDIT` are rewritten by `scripts/regen.sh`:

- To change the models or the method list, change the generator in `codegen/generate.mjs`, run `scripts/regen.sh`
  and commit both.
- If the API itself is wrong or missing something, open an issue: the fix belongs in the API, and the clients pick it
  up on the next weekly regeneration.

Hand-written code (transport, retries, errors, pagination, webhooks, the CLI and MCP server) is edited directly.

## Making a change

1. Fork the repository and create a branch from `main`.
2. Make your change with tests. Keep it focused: one fix or feature per pull request.
3. Run the checks from the repository's README (build, type check, tests). CI runs the same on every pull request.
4. Open a pull request and fill in the template. A maintainer reviews it; CI must be green before merge.

Commit messages: short imperative summary line (`Fix retry on 503 without retry-after`), details in the body if needed.

## Releases

Maintainers release by pushing a `vX.Y.Z` tag after bumping the version in every place `scripts/check-version.sh`
checks. The release workflow verifies the tag, runs the tests, publishes (npm with provenance, PyPI with trusted
publishing; Go is served by the module proxy from the tag) and creates the GitHub Release.

## License

By contributing you agree that your contributions are licensed under the repository's MIT license.
