# app-farm-privacy

GitHub Pages site hosting privacy + support pages for App Farm apps.

Served at: https://sensualodin.github.io/app-farm-privacy/

## Adding a new app

From inside the App Farm framework:

```bash
framework/scripts/generate-privacy.sh <AppName> support@example.com
```

That writes `privacy.md` and `support.md` into `apps/<AppName>/`. Drop them in here:

```bash
# from this repo's root
mkdir -p <appname-lc>/privacy <appname-lc>/support
cp /path/to/apps/<AppName>/privacy.md  <appname-lc>/privacy/index.md
cp /path/to/apps/<AppName>/support.md  <appname-lc>/support/index.md
git add . && git commit -m "<AppName> privacy + support" && git push
```

URLs become:
- `https://sensualodin.github.io/app-farm-privacy/<appname-lc>/privacy/`
- `https://sensualodin.github.io/app-farm-privacy/<appname-lc>/support/`
