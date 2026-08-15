# Angee base addons

This source repository contains the standard Angee addon folders. Each addon
lives under `addons/angee/<name>`, declares its contract in `addon.toml`, and may
carry Python, resources, permissions, and a colocated `web/` fragment.

The repository is a development environment, not a Python distribution. Its
Python dependencies resolve through the sibling editable `django-angee`
checkout.

Run the checks from this directory:

```sh
uv run pytest -q
pnpm install
pnpm -r typecheck
pnpm -r test
```
