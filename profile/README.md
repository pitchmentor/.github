<p align="center">
  <a href="https://pitchmentor.net"><img src="https://cdn.pitchmentor.net/static/logo.png" alt="Pitch Mentor" width="96" height="96"></a>
</p>

<h1 align="center">Pitch Mentor</h1>

<p align="center">
  <b>Real-time AI sales coaching, live on every call.</b><br>
  Official SDKs, CLI and MCP server for the Pitch Mentor API.
</p>

<p align="center">
  <a href="https://pitchmentor.net">Website</a> ·
  <a href="https://pitchmentor.net/docs">API docs</a> ·
  <a href="https://pitchmentor.net/status">Status</a> ·
  <a href="https://discord.gg/SkcxVEJ6wQ">Discord</a>
</p>

---

### Build on Pitch Mentor

Every client is generated from the live [OpenAPI spec](https://api.pitchmentor.net/v1/openapi.json) and covers the
whole API: calls, leads, analytics, team settings, billing, webhooks and API keys. They share the same behavior everywhere: API-key
auth, cursor pagination helpers, automatic retries with idempotency keys, typed errors and webhook signature verification.

| Repository | Install | Version | CI |
|---|---|---|---|
| [**pitchmentor-node**](https://github.com/pitchmentor/pitchmentor-node)<br><sub>TypeScript / JavaScript SDK</sub> | `npm install @pitchmentor/sdk` | [![npm](https://img.shields.io/npm/v/@pitchmentor/sdk?logo=npm&label=npm&color=cb3837)](https://www.npmjs.com/package/@pitchmentor/sdk) | [![CI](https://github.com/pitchmentor/pitchmentor-node/actions/workflows/ci.yml/badge.svg)](https://github.com/pitchmentor/pitchmentor-node/actions/workflows/ci.yml) |
| [**pitchmentor-python**](https://github.com/pitchmentor/pitchmentor-python)<br><sub>Python SDK</sub> | `pip install pitchmentor` | [![PyPI](https://img.shields.io/pypi/v/pitchmentor?logo=pypi&logoColor=white&label=pypi&color=3775a9)](https://pypi.org/project/pitchmentor/) | [![CI](https://github.com/pitchmentor/pitchmentor-python/actions/workflows/ci.yml/badge.svg)](https://github.com/pitchmentor/pitchmentor-python/actions/workflows/ci.yml) |
| [**pitchmentor-go**](https://github.com/pitchmentor/pitchmentor-go)<br><sub>Go SDK</sub> | `go get github.com/pitchmentor/pitchmentor-go` | [![Go Reference](https://pkg.go.dev/badge/github.com/pitchmentor/pitchmentor-go.svg)](https://pkg.go.dev/github.com/pitchmentor/pitchmentor-go) | [![CI](https://github.com/pitchmentor/pitchmentor-go/actions/workflows/ci.yml/badge.svg)](https://github.com/pitchmentor/pitchmentor-go/actions/workflows/ci.yml) |
| [**pitchmentor-cli**](https://github.com/pitchmentor/pitchmentor-cli)<br><sub>Command-line tool</sub> | `npm install -g @pitchmentor/cli` | [![npm](https://img.shields.io/npm/v/@pitchmentor/cli?logo=npm&label=npm&color=cb3837)](https://www.npmjs.com/package/@pitchmentor/cli) | [![CI](https://github.com/pitchmentor/pitchmentor-cli/actions/workflows/ci.yml/badge.svg)](https://github.com/pitchmentor/pitchmentor-cli/actions/workflows/ci.yml) |
| [**pitchmentor-mcp**](https://github.com/pitchmentor/pitchmentor-mcp)<br><sub>MCP server for AI assistants</sub> | `npx -y @pitchmentor/mcp` | [![npm](https://img.shields.io/npm/v/@pitchmentor/mcp?logo=npm&label=npm&color=cb3837)](https://www.npmjs.com/package/@pitchmentor/mcp) | [![CI](https://github.com/pitchmentor/pitchmentor-mcp/actions/workflows/ci.yml/badge.svg)](https://github.com/pitchmentor/pitchmentor-mcp/actions/workflows/ci.yml) |

### Quick start

Create a team API key in the [Pitch Mentor dashboard](https://pitchmentor.net/dashboard/settings) (Settings → Developer), then:

```bash
export PITCHMENTOR_API_KEY=pm_live_...
npx @pitchmentor/cli calls list --period 7d --limit 5
```

### Get help

- **Questions and ideas:** join us on [Discord](https://discord.gg/SkcxVEJ6wQ)
- **Bugs in a client:** open an issue in its repository
- **Security issues:** please follow our [security policy](https://github.com/pitchmentor/.github/blob/main/SECURITY.md), not a public issue

<sub>All clients are open source under the MIT license. npm packages are published with
<a href="https://docs.npmjs.com/generating-provenance-statements">provenance</a> from GitHub Actions.</sub>
