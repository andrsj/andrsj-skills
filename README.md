# andrsj-skills

A [Claude Code plugin marketplace](https://code.claude.com/docs/en/plugin-marketplaces) hub for skills authored by [Andrii Derkach](https://github.com/andrsj). This repo itself ships no code — it's a thin manifest that points at individual plugin repos so they can be installed together under one namespace.

## Install the marketplace

Inside any Claude Code session:

```text
/plugin marketplace add andrsj/andrsj-skills
```

Then install any of the plugins below individually:

```text
/plugin install google-go-styleguide@andrsj-skills
/plugin install go-proverbs-review@andrsj-skills
/reload-plugins
```

Keep everything current with:

```text
/plugin marketplace update andrsj-skills
```

## Plugins in this marketplace

| Plugin | Repo | What it does |
|---|---|---|
| `google-go-styleguide` | [andrsj/google-go-styleguide](https://github.com/andrsj/google-go-styleguide) | Three skills that review Go code against Google's Go Style Guide framework (Style Guide, Style Decisions, Best Practices). Parallel per-rule subagent fan-out. Explicit-only. |
| `go-proverbs-review` | [andrsj/go-proverbs-review-skill](https://github.com/andrsj/go-proverbs-review-skill) | Reviews Go code against Rob Pike's 19 Go Proverbs. Parallel per-proverb subagent fan-out. Activates on explicit request or whenever `.go` files are reviewed. |

## Why a separate hub repo

Following Anthropic's [official marketplace guidance](https://code.claude.com/docs/en/plugin-marketplaces): plugin repos should stay pure (only `.claude-plugin/plugin.json`), and a dedicated marketplace repo should list them via external `github` sources. This keeps each plugin repo focused on its own code and lets the marketplace evolve independently (add/remove plugins without touching their repos).

## License

MIT — see [LICENSE](LICENSE).
