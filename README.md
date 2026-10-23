# codex-plugins

A small Codex plugin marketplace from Eric Eaglstun. One shelf, currently holding one thing.

## Install

```sh
codex plugin marketplace add eaglstun/codex-plugins --ref main
codex plugin add beaglebros@eaglstun
```

To pick up new versions later:

```sh
codex plugin marketplace upgrade eaglstun
```

## Plugins

| Plugin                              | What it does                                                                                                                                      | Source                                                                    |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| [`beaglebros`](plugins/beaglebros/) | Warm, witty, user-respecting product voice for docs, CLI/UI copy, error messages, and design gut checks, after the 1980s Apple II software house. | [eaglstun/skill-beaglebros](https://github.com/eaglstun/skill-beaglebros) |

Each plugin under `plugins/` is a vendored copy of a release from its source
repository. Fix things upstream, not here.

## License

MIT. Each plugin carries its own `LICENSE` as well. Beagle Bros is an independent, unofficial
homage and is not affiliated with or endorsed by the original company.
