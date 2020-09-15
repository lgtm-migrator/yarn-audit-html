# yarn-audit-html

![](https://img.shields.io/david/davityavryan/yarn-audit-html.svg?style=flat-square)
![](https://img.shields.io/david/dev/davityavryan/yarn-audit-html.svg?style=flat-square)
![](https://img.shields.io/david/peer/davityavryan/yarn-audit-html.svg?style=flat-square)
![](https://img.shields.io/github/last-commit/davityavryan/yarn-audit-html.svg?style=flat-square)
![](https://img.shields.io/snyk/vulnerabilities/npm/yarn-audit-html.svg?style=flat-square)
[![](https://img.shields.io/lgtm/alerts/g/davityavryan/yarn-audit-html.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/davityavryan/yarn-audit-html/alerts/)
[![Language grade: JavaScript](https://img.shields.io/lgtm/grade/javascript/g/davityavryan/yarn-audit-html.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/davityavryan/yarn-audit-html/context:javascript)
[![](https://flat.badgen.net/packagephobia/install/yarn-audit-html)](https://packagephobia.now.sh/result?p=yarn-audit-html)

## Generate a HTML report for Yarn Audit

## Install

```bash
yarn global add yarn-audit-html
```

## Usage

To generate a report, run the following:

```bash
yarn audit --json | yarn-audit-html
```

By default the report will be saved to `yarn-audit.html`

If you want to specify the output file, add the `--output` option:

```bash
yarn audit --json | yarn-audit-html --output report.html
```

Unique vulnerability list will be generated by default (Grouped by `MODULE_NAME`, `VERISON` and `CWE`). If you want to show all, one-by-one, add the `--no-unique` option:

```bash
yarn audit --json | yarn-audit-html --no-unique
```

You can also fully customize the generated report by providing `--template` option followed by your own EJS template: 

```bash
yarn audit --json | yarn-audit-html --template ./my-awesome-template.ejs
```

If you'd like the generator to exit with non-zero exit code when vulnerabilities are found, you can add the `--fatal-exit-code` option:
```bash
yarn audit --json | yarn-audit-html --fatal-exit-code
```

Inspired by [npm-audit-html](https://github.com/Filiosoft/npm-audit-html) package.

## License

[MIT](LICENSE.md)
