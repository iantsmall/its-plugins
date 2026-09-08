# its-plugins

Personal Claude Code plugins, distributed as a [plugin marketplace](https://code.claude.com/docs/en/plugin-marketplaces.md) so they're usable across any project or organization, not just one company's tooling.

## Install

In any Claude Code session:

```
/plugin marketplace add iantsmall/its-plugins
/plugin install marquet-playbook@its-plugins
```

The marketplace add is a one-time step per machine. After that, install any plugin from the catalog by name.

To pick up new plugins or updated versions later:

```
/plugin marketplace update
```

## Available plugins

| Name | What it does |
| ---- | ------------ |
| `marquet-playbook` | Shared Claude working-practice guidance, mostly based on the Marquet leadership-language framework (*Turn the Ship Around*, *Leadership Is Language*) — one skill per play: `control-the-clock`, `collaborate-not-coerce`, `commit-not-comply`, `complete-not-continue`, `improve-not-prove`, `connect-not-conform`, `intent-language`, plus `marquet-plays-overview` as a self-triggering index. Also carries `speak-plainly`, a separate personal practice (not from Marquet) for plain, accessible output. Each play self-invokes on its own trigger conditions, so it works ambiently across whatever else Claude is doing — no explicit setup per project. |

## Repository layout

```
its-plugins/
├── .claude-plugin/
│   └── marketplace.json          # Catalog of all plugins in this repo
├── plugins/
│   └── marquet-playbook/
│       ├── .claude-plugin/
│       │   └── plugin.json       # Per-plugin manifest
│       └── skills/
│           └── control-the-clock/
│               └── SKILL.md      # One skill per play
└── README.md
```

## Adding a new plugin

1. Create `plugins/<plugin-name>/` with its own `.claude-plugin/plugin.json` manifest.
2. Put the actual content (`skills/`, `commands/`, `agents/`, `hooks/`, etc.) underneath.
3. Add an entry to the `plugins` array in `.claude-plugin/marketplace.json`.
4. Bump `version` in the plugin's manifest if it's an update to an existing plugin.
5. Add a row to the "Available plugins" table above.
6. Push to `main`. Anyone with this marketplace added picks it up with `/plugin marketplace update`.

Plugin names should be lowercase-kebab-case and descriptive. The marketplace, plugin, and skill names can all be the same when a plugin contains a single skill.

## Keeping plugin descriptions in sync (house rule)

Every plugin's `plugin.json` description must match its `marketplace.json` entry, word for word — pick whichever is more complete, copy it into the other, don't author two independent restatements. A longer SKILL.md frontmatter description can carry more (trigger phrases, scope boundaries) without needing to match verbatim, but it shouldn't contradict the short one either.

## Versioning

Follow semver-ish:
- `0.x.y` while a plugin is new and the behavior may change
- `1.0.0` once it's stable and relied on
- Bump minor for new features, patch for fixes

There's no enforcement — the version field is informational. Updates flow through `/plugin marketplace update` regardless.

## Provenance

`marquet-playbook` started life as `vinemeds-playbook`, built and used inside [VineMeds](https://github.com/VineMeds)'s internal `claude-plugins` marketplace. It moved here since it's personal working-practice guidance rather than VineMeds-specific engineering tooling — nothing in it is company-specific, so it belongs somewhere usable across any project.

`speak-plainly` started life as a standalone personal skill (`eli5`), folded in here because it's the same kind of guidance (how to communicate) even though it isn't sourced from Marquet's framework.
