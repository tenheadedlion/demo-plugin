oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g demo-plugin
$ demo-plugin COMMAND
running command...
$ demo-plugin (--version)
demo-plugin/0.0.0 linux-x64 node-v16.17.0
$ demo-plugin --help [COMMAND]
USAGE
  $ demo-plugin COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`demo-plugin hello PERSON`](#demo-plugin-hello-person)
* [`demo-plugin hello world`](#demo-plugin-hello-world)
* [`demo-plugin help [COMMAND]`](#demo-plugin-help-command)
* [`demo-plugin plugins`](#demo-plugin-plugins)
* [`demo-plugin plugins:install PLUGIN...`](#demo-plugin-pluginsinstall-plugin)
* [`demo-plugin plugins:inspect PLUGIN...`](#demo-plugin-pluginsinspect-plugin)
* [`demo-plugin plugins:install PLUGIN...`](#demo-plugin-pluginsinstall-plugin-1)
* [`demo-plugin plugins:link PLUGIN`](#demo-plugin-pluginslink-plugin)
* [`demo-plugin plugins:uninstall PLUGIN...`](#demo-plugin-pluginsuninstall-plugin)
* [`demo-plugin plugins:uninstall PLUGIN...`](#demo-plugin-pluginsuninstall-plugin-1)
* [`demo-plugin plugins:uninstall PLUGIN...`](#demo-plugin-pluginsuninstall-plugin-2)
* [`demo-plugin plugins update`](#demo-plugin-plugins-update)

## `demo-plugin hello PERSON`

Say hello

```
USAGE
  $ demo-plugin hello [PERSON] -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/Workspace4/hello-world/blob/v0.0.0/dist/commands/hello/index.ts)_

## `demo-plugin hello world`

Say hello world

```
USAGE
  $ demo-plugin hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ demo-plugin hello world
  hello world! (./src/commands/hello/world.ts)
```

## `demo-plugin help [COMMAND]`

Display help for demo-plugin.

```
USAGE
  $ demo-plugin help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for demo-plugin.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.19/src/commands/help.ts)_

## `demo-plugin plugins`

List installed plugins.

```
USAGE
  $ demo-plugin plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ demo-plugin plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.1.7/src/commands/plugins/index.ts)_

## `demo-plugin plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ demo-plugin plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ demo-plugin plugins add

EXAMPLES
  $ demo-plugin plugins:install myplugin 

  $ demo-plugin plugins:install https://github.com/someuser/someplugin

  $ demo-plugin plugins:install someuser/someplugin
```

## `demo-plugin plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ demo-plugin plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ demo-plugin plugins:inspect myplugin
```

## `demo-plugin plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ demo-plugin plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ demo-plugin plugins add

EXAMPLES
  $ demo-plugin plugins:install myplugin 

  $ demo-plugin plugins:install https://github.com/someuser/someplugin

  $ demo-plugin plugins:install someuser/someplugin
```

## `demo-plugin plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ demo-plugin plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ demo-plugin plugins:link myplugin
```

## `demo-plugin plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ demo-plugin plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ demo-plugin plugins unlink
  $ demo-plugin plugins remove
```

## `demo-plugin plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ demo-plugin plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ demo-plugin plugins unlink
  $ demo-plugin plugins remove
```

## `demo-plugin plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ demo-plugin plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ demo-plugin plugins unlink
  $ demo-plugin plugins remove
```

## `demo-plugin plugins update`

Update installed plugins.

```
USAGE
  $ demo-plugin plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
