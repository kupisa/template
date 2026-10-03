# Kupiša template

The start of a repository of themes and modules made for particular sites of the Kupiša platform. Make a
repository of your own from it ("Use this template"), then:

```
composer install
```

That brings the [Kupiša SDK](https://github.com/kupisa/sdk) into `vendor/kupisa/sdk/`: the guides, an example
theme, the public classes of the platform and the views a theme replaces. Open the repository with your AI
assistant and ask for a theme; `AGENTS.md` tells it where everything is.

| Path | What it holds |
|---|---|
| `themes/<name>/` | Your themes, one directory each. |
| `modules/<name>/` | Your modules, one directory each. |
| `AGENTS.md` | What your AI assistant reads first. Set the namespace of the repository there. |
| `CLAUDE.md` | Points Claude Code to `AGENTS.md` and to the rules of the SDK. |

## Checking the code

```
vendor/bin/phpstan
```

checks every theme against the public classes of the platform, so a call to something the platform does not
offer is found before the code reaches a server. It runs on every push too (`.github/workflows/check.yml`).

## Seeing it on a site

```
vendor/bin/kupisa connect
vendor/bin/kupisa dev
```

`connect` asks for the host name of your site and for your SSH key, once. `dev` then uploads your themes and
modules and keeps uploading every file as you save it; `vendor/bin/kupisa push` uploads once. The
[README of the SDK](https://github.com/kupisa/sdk#the-command-line-tool) has every command.

## Keeping up with the platform

```
composer update
```

brings the SDK of the latest release of the platform.
