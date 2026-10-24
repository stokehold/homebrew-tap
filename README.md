# stokehold/homebrew-tap

The Homebrew tap of the stokehold tools.

```sh
brew install stokehold/tap/workflint
```

| Formula | Tool |
| --- | --- |
| `workflint` | [workflint](https://github.com/stokehold/workflint), a linter for GitHub Actions workflows that is compatible with actionlint |

The formulae install the binaries of each tool's GitHub release. They are formulae, not casks, so macOS does not quarantine the binaries.

## How the formulae change

Each workflint release opens a pull request here, `workflint <version>`, from the release workflow of stokehold/workflint. That workflow writes `Formula/workflint.rb` from `packaging/homebrew/workflint.rb.tmpl` in its own repository, so change the template there, not the formula here. The pull request merges itself when `tests.yml` passes.

`tests.yml` runs on every pull request on macOS on Apple silicon, macOS on Intel, and Ubuntu. It taps this checkout as `stokehold/tap` and runs `brew style`, `brew audit --strict`, `brew install`, and `brew test` on each formula.

## License

MIT. See [LICENSE](LICENSE).
