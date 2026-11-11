# qbox-fjord

Public development workspace for a FiveM Qbox server.

## Project status

This repository is being used to organise the source-controlled parts of a local Windows FiveM development server. FXServer runtime files, live configuration, credentials, caches, and backups stay outside the repository.

## Getting started

1. Read [Development layout](docs/DEVELOPMENT_LAYOUT.md).
2. Prepare the local Windows folder structure.
3. Install FXServer artifacts and txAdmin separately from this repository.
4. Set up MariaDB and the Qbox server data using the official Qbox installation instructions.
5. Copy [server.cfg.example](server.cfg.example) to your local server data folder as `server.cfg`, then fill in your own credentials locally.

## Security

This repository is public. Never commit a Cfx.re license key, database password, connection string, webhook, API token, private resource, or live server configuration. The root `.gitignore` excludes common secret/config and runtime paths, but always review files before committing.

## Important

This repository currently provides project organisation and safe configuration examples; it does not contain a complete, ready-to-run Qbox server installation. Follow the official Qbox documentation for the current installation steps and dependencies.
