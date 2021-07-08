<!-- markdownlint-disable MD033 -->
<!-- markdownlint-disable-next-line -->

<h2 align="center">
  <br>
  <p align="center"><img width=30% src="https://raw.githubusercontent.com/kha7iq/subvars/master/.github/img/logo.png"></p>
</h2>

<p align="center">
   <a href="https://github.com/kha7iq/subvars/releases">
   <img alt="Release" src="https://img.shields.io/github/v/release/kha7iq/subvars">
   <a href="https://goreportcard.com/report/github.com/kha7iq/subvars">
   <img alt="Go Report Card" src="https://goreportcard.com/badge/github.com/kha7iq/subvars">
   <a href="#">
   <img alt="Build" src="https://img.shields.io/github/workflow/status/kha7iq/subvars/build">
   <a href="https://github.com/kha7iq/subvars/issues">
   <img alt="GitHub issues" src="https://img.shields.io/github/issues/kha7iq/subvars?style=flat-square&logo=github&logoColor=white">
   <a href="https://github.com/kha7iq/subvars/blob/master/LICENSE.md">
   <img alt="License" src="https://img.shields.io/github/license/kha7iq/subvars">
   <a href="https://pkg.go.dev/github.com/kha7iq/subvars">
   <img alt="Go Dev Reference" src="https://img.shields.io/badge/go.dev-reference-007d9c?logo=go&logoColor=white&style=flat">
</p>

<p align="center">
  <a href="https://kha7iq.github.io/subvars">Documentation</a> •
  <a href="#installation">Install</a> •
  <a href="#configuration">Configuration</a> •
  <a href="#contributing">Contributing</a> •
  <a href="#show-your-support">Show Your Support</a>
</p>

---

## About
Substitute Variables (subvars) is a small utility which provides a way to render any [Go templates](https://golang.org/pkg/text/template/) from command line recognizing the object being passed in and drawing attributes from the object to create wanted text. It is very useful for template driven configuration files.

It uses [sprig v3](https://github.com/Masterminds/sprig) for [template functions](https://masterminds.github.io/sprig) which provides additional functions apart from standard library.

## Installation

### MacOS & Linux Homebrew

```bash
brew install kha7iq/tap/subvars
```

### Linux Binary

```bash
export SUBVARS_VERSION="0.1.0"
wget -q https://github.com/kha7iq/subvars/releases/download/v${SUBVARS_VERSION}/subvars_Darwin_x86_64.tar.gz
tar -xf subvars_Darwin_x86_64.tar.gz
chmod +x subvars
sudo mv subvars /usr/local/bin/subvars
```

### Go Get

```bash
go get -u github.com/kha7iq/subvars
```

### Windows

```powershell
scoop bucket add subvars https://github.com/kha7iq/scoop-bucket.git
scoop install subvars
```

Alternatively you can head over to [release pages](https://github.com/kha7iq/subvars/releases)
and download the binary for windows & all other supported platforms.

### Docker

Docker container is also available `latest` tage will always pull the latest version avaialbe.
You can also download a specific version. Checkout [release](https://github.com/kha7iq/subvars/releases)
page for available versions.

Run Container

```bash
docker pull khaliq/subvars:latest

docker run -it --rm khaliq/subvars:latest --help
```

Usage examples for workflow are available in the repo.

## Usage

```bash
❯ subvars

NAME:
   subvars - Substitute environment variables defined as go templates.

USAGE:
   subvars [global options] command [command options] [arguments...]

VERSION:
   0.1.0

COMMANDS:
   dir, d   Directory lets you render all files in a folder & subfolder.
   help, h  Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --prefix value, --pr value    Match only variables with given prefix pattern [$SUBVARS_PREFIX]
   --missingkey value, -m value  Behavior for missing key when parsing variables. Available options 'invalid', 'error' or 'zero' (default: "invalid") [$SUBVARS_MISSINGKEY]
   --help, -h                    show help (default: false)
   --version, -v                 print the version (default: false)
```

Check [Documentation Page](https://subvars.lmno.pk) for more details.

## Configuration

All the flags have corresponding environment variables associated with it. You
can either provide the value with flags or export to a variable.

View the [Documentation Page](https://subvars.lmno.pk) for more
details.


## Contributing

Contributions, issues and feature requests are most welcome!<br/>Feel free to check
[issues page](https://github.com/kha7iq/subvars/issues). You can also take a look
at the [contributing guide](https://github.com/kha7iq/subvars/blob/master/CONTRIBUTING.md).

## Show your support

Give a ⭐️  if you like this project!

Fork it ⚙️

Make it better 🕶️

## Acknowledgments

This tool was inspired by the orignal [python envtpl](https://github.com/andreasjansson/envtpl) project and [subfuzion/envtpl](https://github.com/subfuzion/envtpl/)
