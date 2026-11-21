# ami-headspace-template

Public **MIT** starter for third-party [ArtificialModularIntelligence](https://github.com/wilfullyapt/ArtificialModularIntelligence) Headspace plugins.

## Install into an AMI appliance

```bash
python -m ami.cli plugin validate .
python -m ami.cli plugin install wilfullyapt/ami-headspace-template@v0.1.0 --enable
# or from a local clone path:
python -m ami.cli plugin install /path/to/ami-headspace-template --enable
```

## Layout

- `plugin.toml` — id, version, ami_api_min, exports
- `__init__.py` — exports `Headspace`, `EXAMPLES`, `__version__`
- `headspace.py` — `@ami_tool` methods (`ping`, `echo`)
- `skills/` — optional seeded markdown skills

## Authoring

1. Fork or copy this repo
2. Change `plugin.toml` `id` / `version`
3. Replace tools in `headspace.py`
4. Tag a release and install with `ami.cli plugin install user/repo@tag`

Contract docs live in the AMI monorepo: `docs/HEADSPACE_PLUGIN.md`, `docs/NEIGHBORS_CONTRACT.md`.
