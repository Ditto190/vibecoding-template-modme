# awesome-copilot Index

This directory is the local cache of reusable assets sourced from
[`Ditto190/awesome-copilot`](https://github.com/Ditto190/awesome-copilot).

## How It Works

- **Canonical source:** `Ditto190/awesome-copilot`
- **Update trigger:** Event-driven on push to `awesome-copilot` (fallback: scheduled refresh)
- **Agents MUST query this index** before authoring a PR or review.

If the index appears stale relative to upstream, note in the PR:

```
Index stale vs upstream; request refresh.
```

## Index Structure

| File | Description |
|------|-------------|
| `index.json` | Machine-readable catalogue of all cached assets |
| `prompts/`   | Cached prompt files from upstream |
| `skills/`    | Cached skill definitions from upstream |
| `checklists/`| Cached review checklists from upstream |

## Refreshing the Index

Run the refresh script (to be implemented as a GitHub Actions workflow) or
manually sync the assets from the upstream repository:

```bash
# Future automation target
gh workflow run refresh-vendor-index.yml
```

Until automation is in place, manually copy updated assets from
`Ditto190/awesome-copilot` into the appropriate subdirectories and update
`index.json` accordingly.
