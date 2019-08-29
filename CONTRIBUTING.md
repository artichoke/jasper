# Contributing to Artichoke

👋 Hi and welcome to [Artichoke](https://github.com/artichoke). Thanks for
taking the time to contribute! 💪💎🙌

The Artichoke project infrastructure is the infrastructure as code for the
[Artichoke Ruby](https://github.com/artichoke/artichoke) project.
[There is lots to do](https://github.com/artichoke/artichoke/issues).

If the Artichoke does not run Ruby source code in the same way that MRI does, it
is a bug and we would appreciate if you
[filed an issue so we can fix it](https://github.com/artichoke/artichoke/issues/new).

If you would like to contribute code 👩‍💻👨‍💻, find an issue that looks interesting
and leave a comment that you're beginning to investigate. If there is no issue,
please file one before beginning to work on a PR.

## Discussion

If you'd like to engage in a discussion outside of GitHub, you can
[join Artichoke's public Discord server](https://discord.gg/QCe2tp2).

## Setup

### Rust

WIP

### Node.js

The Artichoke project infrastructure uses Yarn and Node.js for linting and
orchestration.

You will need to install
[Node.js](https://nodejs.org/en/download/package-manager/) and
[Yarn](https://yarnpkg.com/en/docs/install).

On macOS, you can install Node.js and Yarn with
[Homebrew](https://docs.brew.sh/Installation):

```shell
brew install node yarn
```

### Node.js Packages

Once you have Yarn installed, you can install the packages specified in
[`package.json`](/package.json) by running:

```shell
yarn install
```

You can check to see that this worked by running `yarn lint` and observing no
errors.

### Shell

The Artichoke project infrastructure uses [shfmt](https://github.com/mvdan/sh)
for formatting and [shellcheck](https://github.com/koalaman/shellcheck) for
linting Shell scripts.

On macOS, you can install shfmt and shellcheck with
[Homebrew](https://docs.brew.sh/Installation):

```shell
brew install shfmt shellcheck
```

## Code Quality

### Linting

Once you [configure a development environment](#setup), run the following to
lint sources:

```shell
yarn lint
```

Merges will be blocked by CI if there are lint errors.

## Updating Dependencies

### Node.js Packages

To see what packages are outdated, you can run `yarn outdated`.

To update Node.js package dependencies run the following command and check in
the updated `yarn.lock` file:

```shell
yarn upgrade
```

If after running `yarn upgrade` there are still outdated packages reported by
`yarn outdated`, there has likely been a major release of a dependency. If you
would like to update the dependency and deal with any breakage, please do;
otherwise, please
[file an issue](https://github.com/artichoke/project-infrastructure/issues/new).

## Code Analysis

### Source Code Statistics

To view statistics about the source code in the Artichoke project
infrastructure, you can run `yarn loc`, which depends on
[loc](https://github.com/cgag/loc). You can install loc by running:

```shell
cargo install loc
```
