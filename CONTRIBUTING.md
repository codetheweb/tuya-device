## Introduction

Thank you for considering contributing to TuyAPI! We welcome all kinds of contributions, whether it's a small README fix or a new feature.

Please take a moment to read through this short guide so both the core maintainers' time and your time can be better utilized.

## What you can do

Really, anything you want that's in the scope of this project (you may also want to check out the [@TuyAPI](https://github.com/tuyaapi) organization for other cool projects you could contribute to).

Some ideas:

- Improve documentation
- Track down bugs
- Write tutorials for new users
- Add a new feature
- Respond to new [issues](https://github.com/codetheweb/tuyapi/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc) that are asking for support and not reporting a bug
- Improve test coverage
- Refactor and clean up existing code

## Expectations

Before making any major changes to a user-facing interface or adding a new feature, please open an [issue](https://github.com/codetheweb/tuyapi/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc) with a description of the changes you're planning on making.  Getting feedback before you begin programming ensures that the maintainers' time as well as yours is used more efficiently.

Before you open a PR, make sure all tests pass (see next section).

## Getting started

You're ready to start programming?  Great, here's what you should do:

1. Fork this repository to your account (click the **Fork** button at the top right).
2. Clone your fork to your computer.
3. Run `npm i` to install dependencies.
4. Make a new branch with `git branch`. If you're adding a new feature, use a `feature-*` prefix (ex. `feature-contributing`). If you're fixing a bug, use a `bugfix-*` prefix. Use your best judgement on anything else.
4. Make your changes. (Tip: you can use a file named `dev.js` as a local playground to test your new code in, since the file is ignored by Git.)
5. Ensure test pass with `npm test`. If you get a lot of style-related errors, consider running `npx xo --fix` to automatically fix most of them.
6. Commit, push, and open a PR to the **development** branch (not master). Expect to hear back within a week or so (usually sooner).
