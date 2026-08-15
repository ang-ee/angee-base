# Angee base addons

This repository owns Angee's standard folder addons under `addons/angee/*`.
An addon is a source folder with an `addon.toml`, not a separately distributed
Python package. Keep each capability, manifest, resources, permissions, and web
fragment together in its owning addon.

The supported layout is a stack workspace slot: this checkout sits at
`<stack>/workspaces/<ws>/angee-base` with `angee-django`, `angee-react`, and
`angee-examples` as sibling slots, and the stack root above owns the composed
host — the `@angee/gql` fixture and generated SDL resolve from the stack root's
`runtime/` (regenerate with `manage.py angee build` + web codegen there). Do
not move addon behavior into the framework core or generated runtime output.

Before handing off changes, run `uv run pytest -q`, `pnpm -r typecheck`, and
`pnpm -r test` from the repository root.
