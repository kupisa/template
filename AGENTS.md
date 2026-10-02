# Themes and modules for the Kupiša platform

This repository holds themes and modules made for particular sites of the Kupiša platform. The rules and the
guides for building them come with the Kupiša SDK. Before any work, read `vendor/kupisa/sdk/AGENTS.md` and
follow it; when `vendor/kupisa/sdk/` is not there, run `composer install` first.

## This repository

- **Namespace:** `sites\template`. It is the path of this repository from the `sites` directory of the platform
  (`sites/template/`). A repository made from the template sits elsewhere: change the namespace here first, to
  `sites\<directory>` (or `sites` alone for a repository that is the `sites` directory itself).
- A theme is `themes/<name>/Theme.php`, the class `sites\template\themes\<name>\Theme`.
