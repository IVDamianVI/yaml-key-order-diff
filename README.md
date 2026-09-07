# YAML Key Order Diff

Lightweight, browser-based tool for comparing YAML files with a focus on **key order consistency**.

Designed primarily for i18n / locale files, where keeping the same key structure across languages
matters for readability and long-term maintenance.

No backend. No dependencies. Just paste and compare.

---

## Features

- Detects **missing and extra keys**, including nested mapping paths
- Highlights **reordered keys and mismatched indentation**
- Marks **identical leaf values** as warnings; different values are allowed
- Preserves Target indentation in Result so formatting errors remain visible
- Previous / next buttons cycle through structural differences and warnings
- Source, Target and Result scroll together vertically and horizontally, including difference navigation
- Separate difference and warning counters; hover a highlighted row for details
- Visual, side-by-side comparison
- Works entirely in the browser

---

## Use cases

- Keeping i18n / locale YAML files in sync
- Reviewing translated configuration files
- Verifying structure consistency between environments
- Manual diffing where standard line-based diff is not enough

---

## How it works

1. Paste the reference YAML file into **Source**
2. Paste the file to compare into **Target**
3. The tool highlights:
   - missing or extra keys
   - reordered keys and different indentation
   - identical values (warnings, including empty leaf values)

The result panel shows a visual diff focused on structure rather than raw text differences.

---

## Limitations

- Supports block-style mappings, nested keys, quoted keys and literal/folded block values
- Does not fully parse YAML: sequences, flow collections, anchors, aliases and complex keys are not structurally interpreted
- Values are compared as text (ignoring surrounding whitespace and inline comments for single-line values), without YAML type or quote normalization
- Blank lines and standalone comments are compared as non-key lines; final line endings are normalized
- Result follows Source key order and appends extra Target keys; structural errors take visual priority over identical-value warnings
- Not a replacement for full YAML parsers or validators

This is a **structural diff helper**, not a YAML linter.

---

## Usage

The tool is a single static HTML file.

You can:
- open it directly in the browser
- embed it into internal tooling

No build step required.

Run comparison regression tests with `node --test comparison.test.cjs`.

---

## License

MIT
