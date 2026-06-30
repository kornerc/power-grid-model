<!--
SPDX-FileCopyrightText: Contributors to the Power Grid Model project <powergridmodel@lfenergy.org>

SPDX-License-Identifier: MPL-2.0
-->

# Development Container Setup Guide

This document explains how you can use our development container (dev container) setup to contribute to the _Python_
side of `power-grid-model`.

```{note}
A [development container](https://containers.dev/) is a pre-configured
[container](https://en.wikipedia.org/wiki/Containerization_(computing)).
It includes all necessary dependencies for an immediate development start.
Most modern IDEs support dev containers natively.
This allows you to use your preferred editor and personal extensions directly inside the isolated environment.
```

## Prerequisites

To start developing in the dev container, you must clone the repository, install a container engine, and _(optionally)_
configure an IDE or editor that supports remote container connections.

First, **clone the repository:**

```shell
git clone https://github.com/PowerGridModel/power-grid-model.git
```

For the container engine and the IDE/editor you have several options:

**Container Engine:**

* [Podman](#podman) _(Recommended)_
* [Docker](#docker)

**IDE/Editor:**

* [Visual Studio Code](#visual-studio-code) _(Fully supported)_
* [PyCharm](#pycharm)
* [Zed](#zed)

## Container Engine

### Podman

[Podman](https://podman.io/) is an open-source container management tool featuring a command-line interface and an
optional graphical user interface called `Podman Desktop`.
Both tools are free for both private _and commercial_ use.
A key security advantage of Podman over other engines is its _rootless_ architecture, meaning it operates entirely
without root (admin) privileges.

* **Installation:** Follow the official guides for [Podman](https://podman.io/docs/installation) _or_
[Podman Desktop](https://podman-desktop.io/docs/installation).
* **Initialization:** If using `Podman Desktop`, open the application and click `initialize and start`.
Once successful, the status will change to a green `RUNNING` indicator.

### Docker

[Docker](https://www.docker.com/) consists of the core `Docker` engine and an optional graphical interface,
`Docker Desktop`.
Note that professional use of Docker Desktop in larger enterprises _requires a paid subscription._

* **Installation:** Follow the official guides for [Docker](https://docs.docker.com/engine/install/) Engine _or_
[Docker Desktop](https://docs.docker.com/get-started/get-docker/).

## IDE/Editor

### Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/docs/devcontainers/containers) offers full, native integration with
development containers.

* Install the [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
  extension.
* Open the cloned `power-grid-model` folder in VS Code.
* Click the green `Remote Indicator` button in the bottom-left corner or open the Command Palette
  (`Ctrl+Shift+P` / `Cmd+Shift+P`)
* Select `Dev Containers: Reopen in Container`.

### PyCharm

[PyCharm Professional](https://www.jetbrains.com/help/pycharm/dev-containers-starting-page.html) provides native support
for development containers.
Note that the _Professional_ edition is required to have native development container support in PyCharm.

* Open the [welcome screen](https://www.jetbrains.com/help/pycharm/welcome-screen.html) of PyCharm.
* Click `Remote Development`, choose `Dev Containers` and click the `Create Dev Containers` button.
* Select your local path to the cloned repository and choose your container engine.

### Zed

[Zed](https://zed.dev/docs/dev-containers) supports development containers via its built-in container integration.

* Ensure your container engine (Podman or Docker) is running.
* Open the cloned `power-grid-model` folder in Zed, a prompt should automatically appear with the option
  `Open in Container`.
  Alternatively, use the command palette (`Ctrl+Shift+P` / `Cmd+Shift+P`) to run `Project: Open Remote` and select
  `Connect Dev Container`
* Follow the prompt to initialize the development container environment.
