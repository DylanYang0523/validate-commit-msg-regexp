# validate-commit-msg-regxep

[![MIT License][license-badge]][LICENSE]
[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors)
[![PRs Welcome][prs-badge]][prs]

## Declaration

This is a project base on [validate-commit-msg](https://github.com/conventional-changelog-archived-repos/validate-commit-msg). The original GitHub code and [npm modules](https://www.npmjs.com/package/validate-commit-msg) had been deprecated (not quite sure will they reuse the code again or not), but if you are one of the original users and also if you like the project, welcome to play and discuss together.

## Features

More RegExp related options you can set for commit message.

## Installation

#### npm

This module is distributed via [npm](https://www.npmjs.com/) which is bundled with [node](https://nodejs.org/) and
should be installed as one of your project's `devDependencies`:

```
npm install --save-dev validate-commit-msg-regxep
```

Now, you can choose one setting option from below.

#### #1 setting option

You can specify options in `.vcmrc` file.
It must be valid JSON file.

```json
{
  "types": [
    "feat", "fix", "docs", "style", "refactor",
    "perf", "test", "build", "ci", "chore", "revert"
  ],
  "scope": {
    "required": false,
    "allowed": ["*"],
    "validate": false,
    "multiple": false,
    "regexpMode": false,
  },
  "warnOnFail": false,
  "maxSubjectLength": 100,
  "subjectPattern": ".+",
  "subjectPatternErrorMsg": "subject does not match subject pattern!",
  "helpMessage": "",
  "autoFix": false
}
```

#### #2 setting option

You can specify options in `package.json` file.
It must be valid JSON file.

```json
{
  "config": {
    "validate-commit-msg": {
      // ... your custom setting here
    }
  }
}
```

## Recommend Using

- [husky](https://www.npmjs.com/package/husky) ⇨ Git hooks made easy. ⭐⭐⭐⭐⭐

```json
// edit package.json
...
{
  "scripts": {
    "...": "...",
    "commitmsg": "validate-commit-msg-regexp",
    "...": "..."
  }
}
...
```
- [commitizen](https://www.npmjs.com/package/commitizen) ⇨ Help you to create a regular commit msg. ⭐⭐⭐

```json
// edit package.json
...
{
  "scripts": {
    "...": "...",
    "commit": "git-cz",
    "...": "..."
  }
}
...
{
  "config": {
    "commitizen": {
      "path": "./node_modules/cz-conventional-changelog"
    }
  }
}
...
```

[license-badge]: https://img.shields.io/npm/l/validate-commit-msg.svg?style=flat-square
[license]: https://github.com/DylanYang0523/validate-commit-msg-regexp/blob/master/LICENSE
[prs-badge]: https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square
[prs]: http://makeapullrequest.com

## Contributors

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
| [<img src="https://avatars0.githubusercontent.com/u/12027934?v=4" width="100px;"/><br /><sub>Dylan Yang</sub>](https://github.com/DylanYang0523)<br /> |
| :---: |
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/kentcdodds/all-contributors) specification. Contributions of any kind welcome!
