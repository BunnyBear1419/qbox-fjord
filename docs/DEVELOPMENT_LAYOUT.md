# Development layout

This repository is the public, version-controlled project workspace. It is not the FXServer installation itself.

## Recommended Windows folders

```text
C:\FiveM-Development\
├── artifacts\       # FXServer artifacts; keep out of Git
├── server-data\     # Live server data and real server.cfg; keep secrets local
├── qbox-fjord\      # This Git repository
└── backups\         # Local backups; never commit database dumps
```

The exact paths can be adjusted during setup. Keep the Git repository separate from downloaded FXServer artifacts and live runtime/cache folders.

## Public repository contents

- Source-controlled custom resources and scripts that you are permitted to publish
- Documentation, installation notes, and SQL schema files
- Example configuration files containing placeholders only

## Keep these local and private

- Your real `server.cfg`
- Cfx.re server registration key
- MariaDB passwords and complete connection strings
- API tokens, webhook URLs, private keys, and personal credentials
- FXServer artifacts, runtime caches, logs, crash dumps, and database backups
- Paid, escrowed, or otherwise private resources unless their licence explicitly permits redistribution

## Configuration workflow

1. Copy `server.cfg.example` to your local server's `server.cfg`.
2. Replace placeholders in the local copy only.
3. Keep the real `server.cfg` outside this repository where possible. The root `.gitignore` also excludes common live config paths.
4. Before every commit, review the changed-file list and search for credentials.

## Important

A public repository means anyone can read and clone its contents. Do not rely on obscurity or on removing a secret later: rotate any credential that is accidentally published.
