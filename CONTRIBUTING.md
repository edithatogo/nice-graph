# Contributing to nice-graph

Contributions improve the NICE technology-appraisal corpus, extraction pipeline, knowledge graph, and web interface while keeping every extracted claim traceable to its source.

## Before you start

Read the [README](README.md), [Python project configuration](pyproject.toml), and [ontology methods](ontology/methods.md). Identify which pipeline stage or entity definition changes, and describe implications for downstream resolution and search.

Search existing issues and pull requests to avoid duplicating work. Describe substantial proposals before implementation, and use repository issue or pull request templates when available. Small corrections can go directly into a focused pull request.

For bug reports, include the affected version or commit, environment, minimal reproduction, expected and actual behavior, and sanitized diagnostics. For feature requests, explain the use case and intended outcome.

## Development and validation

The README uses `uv sync` to prepare the Python environment. The supported interpreter is declared in `pyproject.toml`; use its requirements and the existing lockfile. The web application's setup is documented separately in the README.

For pipeline changes, use small public or synthetic fixtures and compare affected extraction or indexing outputs with expected results. Preserve source identifiers, page markers, extraction provenance, and the distinction between company, assessment-group, and committee positions. Document schema migrations or index rebuilds explicitly.

The current project configuration does not declare an automated test suite. Record the validation you actually performed rather than inventing a test command. Full corpus rebuilding can involve downloads and external model calls; use a bounded, explicitly configured run and keep API keys out of source and logs.

Update affected documentation and examples alongside behavior changes. Add a focused regression case for a bug fix where executable tests are appropriate. Record checks that were not run and the reason.

## Submitting a pull request

Create a focused branch from the current `main` branch and open a pull request back to it. Keep unrelated formatting, refactoring, and dependency changes separate.

Include:

- The problem, proposed change, and resulting behavior.
- Related issues or existing track references.
- Exact validation commands or inspection steps, results, and limitations.
- Compatibility implications and any data or dependency provenance.

Inspect the complete diff before submission. Required automated checks must pass before merge. Follow the existing repository and account policies; this guide does not introduce a second-person approval requirement or relax existing checks.

## Security and sensitive information

Follow the [account security policy](https://github.com/edithatogo/.github/blob/main/SECURITY.md). Report vulnerabilities privately through GitHub's **Report a vulnerability** option if available. Otherwise request a private reporting contact without disclosing the vulnerability publicly. Keep credentials, personal data, and unredacted logs out of commits, issues, and examples.

## Licensing and conduct

Respect the [existing license](LICENSE) and preserve third-party notices. Submit only material you are entitled to contribute, and document unclear permissions before adding third-party content. Follow the [account code of conduct](https://github.com/edithatogo/.github/blob/main/CODE_OF_CONDUCT.md). This guide adds no CLA, mandatory sign-off, or relicensing condition.

## Reference guidance

- [GitHub contributor guidelines](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors)
- [OpenSSF Best Practices criteria](https://www.bestpractices.dev/en/criteria)
