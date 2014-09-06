repository
==========

Checkout a git repository and compile it or link it

[![Build Status](https://travis-ci.org/osxc/repository.svg)](https://travis-ci.org/osxc/repository/)

## Requirements

- XCode Command-Line Tools (needs `git` and the build tools)
- Sudo permissions for installing the build

> **Note:** This role is generic enough to be used from a Linux distribution if you've got `git` and the build tools installed.

## Role variables

| Name                  | Description                                      | Default            |
|-----------------------|--------------------------------------------------|--------------------|
| `clone_url`           | Where to clone from ?                            | none, required     |
| `dest`                | Destination path (locally)                       | none, required     |
| `version`             | The version to checkout                          | `HEAD`             |
| `links`               | Array of dicts to create symbolic links: `{src: "relative/to/the/root/of/the/git/repo", dest: "/relative/to/root or ~/your/home"}` | `[]` |
| `env`                 | Array of dicts to inject env: `{regex: "^export VAR_NAME", line: "export VAR_NAME='value'"}` | `[]` |
| `build`               | Do you want to build this repo ?                 | `false`            |
| `configure_cmd`       | The build configuration command                  | `./configure`      |
| `build_cmd`           | The build command                                | `make`             |
| `install_cmd`         | The installation command                         | `make install`     |

## Dependencies

- osxc.common_env

## License

MIT

## Author

- Robin Ricard

