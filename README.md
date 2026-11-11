# claude-plugins

My [Claude Code](https://code.claude.com) plugins, as a marketplace. To add it with auto-update on
and install `reddit`, run this in a terminal (needs `jq`):

```bash
claude plugin marketplace add adigourdi/claude-plugins &&
jq '.extraKnownMarketplaces["adigourdi"].autoUpdate = true' ~/.claude/settings.json > ~/.claude/settings.json.new &&
mv ~/.claude/settings.json.new ~/.claude/settings.json &&
claude plugin install reddit@adigourdi
```

Plugins install for all your projects. New versions arrive in the background and load at your next
launch; to update right away, run `claude plugin update reddit@adigourdi`.

| Plugin | What it does |
|--------|--------------|
| [reddit](plugins/reddit) | Search Reddit and digest threads, read-only, through a local Chrome window. No API key or account. |

## License

[MIT](LICENSE)
