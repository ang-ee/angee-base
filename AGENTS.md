# Angee base addons

This repository owns Angee's standard folder addons under `addons/angee/*`.
An addon is a source folder with an `addon.toml`, not a separately distributed
Python package. Keep each capability, manifest, resources, permissions, and web
fragment together in its owning addon.

The supported sibling layout places `angee-django` and `angee-react` beside this
checkout. Do not move addon behavior into the framework core or generated
runtime output.

Before handing off changes, run `uv run pytest -q`, `pnpm -r typecheck`, and
`pnpm -r test` from the repository root.
