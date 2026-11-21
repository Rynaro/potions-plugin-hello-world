# Potions Plugin Hello World

A small example plugin for Potions. It adds a `hello-world` shell command that confirms the plugin loaded and points to a next step. It is a Potions counterpart to Docker's Hello World example and does not use Docker.

## Install

This plugin requires Potions 2.18.0 or later. Review the repository and resolved commit when Potions asks for trust. Its shell configuration runs with your account permissions.

Install directly from its tagged GitHub repository:

```sh
potions plugin install Rynaro/potions-plugin-hello-world@v1.0.0
```

After its entry appears in Potions Shelf, you can also install it by its catalog name:

```sh
potions plugin install plugin-hello-world
```

Open a new Zsh shell, then run:

```sh
hello-world
```

Expected output:

```text
Hello from Potions!
This plugin loaded in your shell.
Try potions plugin search shell to discover more.
```

The command prints this greeting when invoked. Sourcing the plugin defines the function without printing anything or making system changes.

## Develop locally

Clone the repository, edit `config/init.zsh`, and create a linked local install:

```sh
git clone https://github.com/Rynaro/potions-plugin-hello-world.git
cd potions-plugin-hello-world
potions plugin validate ./
potions plugin install ./
```

Open a new shell to try your changes. Local installs point to your checkout, so edits are picked up in new shells.

Disable or re-enable the plugin from Potions Desk or the terminal menu:

```sh
potions plugin deactivate plugin-hello-world
potions plugin activate plugin-hello-world
```

To uninstall it:

```sh
potions plugin uninstall plugin-hello-world
```

Uninstalling a local plugin removes its Potions link and preserves the cloned repository.

## License

MIT. See [LICENSE](LICENSE).
