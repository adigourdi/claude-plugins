# claude-plugins

My [Claude Code](https://code.claude.com) plugins, as a marketplace. In a terminal:

```bash
claude plugin marketplace add adigourdi/claude-plugins
claude plugin install reddit@adigourdi
```

Plugins install for all your projects.

## Auto-update (optional)

Updates are off by default. To turn them on (needs `jq`):

```bash
jq '.extraKnownMarketplaces["adigourdi"].autoUpdate = true' ~/.claude/settings.json > ~/.claude/settings.json.new &&
mv ~/.claude/settings.json.new ~/.claude/settings.json
```

In Claude Code, `/plugin` → **Marketplaces** → **adigourdi** → **Enable auto-update** does the same.
New versions then arrive in the background and load at your next launch. To update by hand:
`claude plugin update reddit@adigourdi`.

| Plugin | What it does |
|--------|--------------|
| [reddit](plugins/reddit) | Search Reddit and digest threads, read-only, through a local Chrome window. No API key or account. |

## License

[MIT](LICENSE)
