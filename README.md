# YAML Key Order Diff

Lightweight, browser-based tool for comparing YAML files with a focus on **key order consistency**.

Designed primarily for i18n / locale files, where keeping the same key structure across languages
matters for readability and long-term maintenance.

No backend. No dependencies. Just paste and compare.

---

## Features

- Detects **missing keys**
- Highlights **moved / reordered keys**
- Marks **unchanged values** with different ordering
- Preserves indentation and formatting
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
   - missing keys
   - keys moved to a different position
   - unchanged values with different ordering

The result panel shows a visual diff focused on structure rather than raw text differences.

---

## Limitations

- Intended for **simple, flat YAML structures**
- Does not fully parse YAML (anchors, complex nesting, multiline values)
- Keys must follow the `key: value` pattern
- Not a replacement for full YAML parsers or validators

This is a **structural diff helper**, not a YAML linter.

---

## Usage

The tool is a single static HTML file.

You can:
- open it directly in the browser
- embed it into internal tooling

No build step required.

---

## License

MIT
