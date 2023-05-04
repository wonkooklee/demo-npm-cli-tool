# Pathmap Generator for 'Pages' directory of Next.js

## Requirements

- node.js >= 14.0.0

## Core dependencies

- [globby](https://github.com/sindresorhus/globby)
- [inquirer](https://github.com/SBoudrias/Inquirer.js)
- [json-format](https://github.com/luizstacio/json-format)

## How to use

npx script running fashion.

```sh
npx demo-npm-cli-tool # cannot define config file.
or
npm install demo-npm-cli-tool
```

## Configuration vs. Cli Interactions

To configure required properties you should define either configuration in `pathmap.config.json` or `via CLI-input`.

### pathmap.config.json

```json
{
  "pathToPages": "src/pages",
  "pathToSave": "path/path.json",
  "includes": ["**/*.page.{ts,tsx}"],
  "excludes": ["!node_modules"], // remember, path expression in excludes must start with exclamation mark.
  "schema": {
    "query": []
    // any key:value pairs..
  }
}
```

### Interactive CLI Dialogs.

```sh
? Enter the path to the '/pages' directory. src/pages
? Enter the destination to save jsonized pathmap file. pathmap/pathmap.json
? includes: **/*.page.{ts,tsx}
? excludes: **/[!_]*.{ts,tsx}, **/[!A-Z]*.page.{ts,tsx}, !api
```

## Result

```json
{
  "/": {
    "alias": "",
    "trackPageView": true,
    "query": []
  },
  "/services/loan": {
    "alias": "",
    "trackPageView": true,
    "query": []
  }
}
```

<br />

© WONKOOK LEE
