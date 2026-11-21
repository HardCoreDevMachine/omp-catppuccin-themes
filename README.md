# Catppuccin themes for OMP

Catppuccin flavor assets for [OMP](https://github.com/YanwuZeng/omp). Install them as custom OMP themes and select a light or dark flavor from the OMP appearance settings.

**Release:** `v1.0.0`

## Included flavors

| Flavor | Recommended slot | Theme name |
| --- | --- | --- |
| Latte | Light | `catppuccin-latte` |
| Frappe | Dark | `catppuccin-frappe` |
| Macchiato | Dark | `catppuccin-macchiato` |
| Mocha | Dark | `catppuccin-mocha` |

Each asset contains the complete Catppuccin palette, OMP UI colors, status-line colors, HTML export colors, and terminal ANSI colors.

## Requirements

- [OMP](https://github.com/YanwuZeng/omp)
- [GNU Stow](https://www.gnu.org/software/stow/)

## Install

From the repository root:

```sh
stow --dir "$PWD" --target "$HOME/.omp" omp
```

Stow creates links under `~/.omp/agent/themes/` for all four theme files.

## Select a flavor

Set the OMP light and dark theme slots in `~/.omp/agent/config.yml`:

```yaml
theme:
  light: catppuccin-latte
  dark: catppuccin-mocha
```

For the dark slot, use `catppuccin-frappe`, `catppuccin-macchiato`, or `catppuccin-mocha`. You can also select an installed flavor from **Settings → Appearance** in OMP.

## Update

Pull the latest files and refresh the links:

```sh
git pull --ff-only
stow --restow --dir "$PWD" --target "$HOME/.omp" omp
```

## Uninstall

From the repository root:

```sh
stow --delete --dir "$PWD" --target "$HOME/.omp" omp
```
