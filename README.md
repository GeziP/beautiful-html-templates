# Quaero Beautiful HTML Templates

Beautiful HTML presentation templates designed for AI-powered deck generation.

30+ production-grade HTML slide templates with Quaero institutional chrome — designed so that any coding agent can pick the right one and produce a beautiful deck on the user's behalf, automatically.

## Get started

Copy this to your coding agent:

```
Clone https://github.com/GeziP/quaero-beautiful-html-templates and follow the instructions in AGENTS.md to build me a beautiful HTML slide deck.
```

Agents using the library should read [`AGENTS.md`](./AGENTS.md). It's the operating manual: how to read `index.json`, match the user's brief to a template, clone it, and adapt the content.

## Quaero Chrome

Every template includes Quaero institutional chrome — a consistent header and footer bar that adapts to each slide's background luminance. The chrome provides:

- Fixed header showing current slide title and page counter
- Footer with Quaero logo and confidentiality notice
- Automatic light/dark text switching based on slide background

## Template Gallery

All templates are organized under `templates/` with this structure:

```
templates/<template-slug>/
  template.html      # Self-contained HTML slide deck
  template.json      # Metadata: mood, tone, palette, best_for
  styles.css         # (optional) External styles
  deck-stage.js      # (optional) Custom slide engine
```

Browse all templates in the [`templates/`](./templates/) folder. Each `template.json` describes the template's visual system, mood, and ideal use case — agents use this metadata to match user briefs to the right template.

## How it works

1. Agent asks user about occasion and mood
2. Agent reads `index.json` and picks 3 matching templates
3. Agent builds title-slide previews for user to compare
4. Agent clones the chosen template and replaces content
5. Agent writes the finished deck to the user's specified location

See [`AGENTS.md`](./AGENTS.md) for the full workflow.

## License

[MIT](./LICENSE) — free to use, modify, and distribute.
