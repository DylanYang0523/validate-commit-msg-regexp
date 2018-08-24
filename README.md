# validate-commit-msg-regexp

[![MIT License][license-badge]][LICENSE]
[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors)
[![PRs Welcome][prs-badge]][prs]

## Declaration

This is a project base on [validate-commit-msg](https://github.com/conventional-changelog-archived-repos/validate-commit-msg). The original GitHub code and [npm modules](https://www.npmjs.com/package/validate-commit-msg) had been deprecated (not quite sure will they reuse the code again or not), but if you are one of the original users and also if you like the project, welcome to play and discuss together.

## Demo

<img src="http://share.gifyoutube.com/nr1DQW.gif" data-canonical-src="http://share.gifyoutube.com/nr1DQW.gif" width="582" height="280" />

## Installation

#### step.1 👉🏻 npm

This module is distributed via [npm](https://www.npmjs.com/) which is bundled with [node](https://nodejs.org/) and
should be installed as one of your project's `devDependencies`:

```
npm install --save-dev validate-commit-msg-regexp
```

Now, you can choose one setting option from below.

#### step.2 👉🏻 configuration

You can create and specify options in `.vcmrc` file.
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
or... you can specify options in your `package.json` file.
It must be valid JSON file, as well.

```json
{
  "config": {
    "validate-commit-msg": {
      // ... your custom setting here
    }
  }
}
```

#### step.3 👉🏻 git hooks

Set this validation mechanism to where ever you want it can collaborate with, like your git hook system. You can read from `Recommend Using`⬇️⬇️⬇️

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

## Options

#### types 🐡

These are the types that are allowed for your commit message. If omitted, the value is what is shown above.

You can also specify: `"types": "*"` to indicate that you don't wish to validate types.

Or you can specify the name of a module that exports types according to the
[conventional-commit-types](https://github.com/commitizen/conventional-commit-types)
spec, e.g. `"types": "conventional-commit-types"`.

#### scope 🐙

This object defines scope requirements for the commit message.

* ***required*** ➡ A boolean to define whether a scope is required for all commit messages.

* ***allowed*** ➡ An array of scopes that are allowed for your commit message. You may also define it as `"*"` which is the default to allow any scope names.

* ***validate*** ➡ A boolean to define whether or not to validate the scope(s) provided.

* ***multiple*** ➡ A boolean to define whether or not to allow multiple scopes.

* ***regexpMode*** ➡ A boolean to define whether or not to validate allowed array with regular expression.

#### warnOnFail 🦄

If this is set to `true` errors will be logged to the console, however the commit will still pass.

#### maxSubjectLength 🐨

This will control the maximum length of the subject.

#### subjectPattern 🐝

Optional, accepts a RegExp to match the commit message subject against.

#### subjectPatternErrorMsg 🐧

If `subjectPattern` is provided, this message will be displayed if the commit message subject does not match the pattern.

#### helpMessage 🐔

If provided, the helpMessage string is displayed when a commit message is not valid. This allows projects to provide a better developer experience for new contributors.

The `helpMessage` also supports interpolating a single `%s` with the original commit message.

#### autoFix 🐳

If this is set to `true`, type will be auto fixed to all lowercase, subject first letter will be lowercased, and the commit will pass (assuming there's nothing else wrong with it).

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
