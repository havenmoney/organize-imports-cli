# organize-imports-cli

> VS Code's '[Organize imports](https://code.visualstudio.com/updates/v1_23#_javascript-and-typescript-organize-imports)' executable from command line

Plays nicely with Prettier and [lint-staged](https://github.com/okonet/lint-staged):

```json
"lint-staged": {
  "*.ts": [
    "organize-imports-cli",
    "prettier --write",
    "git add"
  ]
}
```

## Usage

```console
> organize-imports-cli files...
```

Files can be specific `ts` and `js` files or `tsconfig.json`, in which case the whole project is processed.

Files containing the substring `// organize-imports-ignore` are skipped.
