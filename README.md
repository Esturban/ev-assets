# ev-assets

Public, hotlink-safe host for social post images.

Why this exists: Google Drive returns 403 to any cross-site Referer even for files shared
with "anyone with the link", so Buffer and LinkedIn render a broken image. raw.githubusercontent.com
serves the correct content-type with no referer check.

## Structure

Two top-level folders, one per asset type. No date or topic subfolders inside `images/` -
the existing filename already encodes what you need to find a file by, so the folder just
holds them flat.

```
ev-assets/
  images/
    <topic-slug>-<platform>[-v<N>].png
  lead-magnets/
    YYYY-MM-DD-<slug>/
      source.html
      <slug>.pdf
```

**`images/`** - flat, one file per asset. Naming rule: `<topic-slug>-<platform>[-v<N>].png`.
- `<topic-slug>` - the post's topic, kebab-case (e.g. `compile-once-run-forever`)
- `<platform>` - `linkedin` or `x`. Omit only for pre-platform-split legacy files.
- `-v<N>` - omit for the first/original version; add `-v2`, `-v3`, ... for later renders of
  the same topic+platform. This is the pattern already in use across the existing 31 files -
  keeping it flat instead of nesting by topic or date, since the slug already makes a file
  findable without opening a folder tree.

**`lead-magnets/`** - one dated-slug subfolder per magnet, unchanged from the existing
convention: `lead-magnets/YYYY-MM-DD-<slug>/` containing `source.html` and the rendered PDF.
Kept as-is rather than reworked, since it already does the job and nothing about `images/`
requires it to match.

## Deriving a servable URL

```
https://raw.githubusercontent.com/Esturban/ev-assets/master/images/<topic-slug>-<platform>[-v<N>].png
https://raw.githubusercontent.com/Esturban/ev-assets/master/lead-magnets/YYYY-MM-DD-<slug>/<filename>
```

Pattern: `https://raw.githubusercontent.com/Esturban/ev-assets/master/<path-from-repo-root>`.
Any tool with the repo-relative path (render pipeline, CMO agent, manual copy-paste) can
build the URL without asking anyone - that's the whole point of the flat, self-describing
naming rule above.
