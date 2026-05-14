# getskibots.com dev

This repository is set up to deploy static page prototypes to `https://getskibots.com/dev/` over SFTP.

## GitHub Actions secrets

Add these in GitHub under `Settings > Secrets and variables > Actions`:

```text
SFTP_HOST=bmk.8e2.myftpupload.com
SFTP_PORT=22
SFTP_USER=<GoDaddy generated username>
SFTP_PASSWORD=<GoDaddy generated password>
SFTP_REMOTE_PATH=/dev
```

Use `SFTP_REMOTE_PATH=/html/dev` instead if GoDaddy's SFTP file browser shows an `html` folder first.

## Deploy scope

The workflow deploys this repository's prototype files to the configured remote path. It intentionally ignores GitHub workflow files, `.git`, `node_modules`, `.env`, and logs.

Put prototypes in the repository root, for example:

```text
index.html
styles.css
main.js
assets/
```
