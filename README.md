# ev-assets

Public, hotlink-safe host for social post images.

Why this exists: Google Drive returns 403 to any cross-site Referer even for files shared
with "anyone with the link", so Buffer and LinkedIn render a broken image. raw.githubusercontent.com
serves the correct content-type with no referer check.
