# Replica Studio CLI

Standalone public distribution of the Replica Studio command-line client.

## Download

Download `replica_cli.py` from the latest GitHub Release.

## Requirements

- Python 3.11 or newer
- `requests`

Install the runtime dependency:

```bash
python3 -m pip install "requests>=2.32,<3"
```

## Usage

```bash
python3 replica_cli.py --help
python3 replica_cli.py login --label "My computer"
python3 replica_cli.py whoami --json
```

The CLI uses device authorization. Complete the approval in an already signed-in
Replica Studio browser session. The token is stored in
`~/.config/replica-studio/cli.json` with owner-only permissions and is never
printed by the login command.

The default server is `https://replica-studio.upupup.today`.

## Security

Do not print, copy, upload, or commit the token file. Paid actions require the
`run` token scope and an explicit `--yes`; deletion requires the `delete` scope
and `--yes`.

This repository contains only the CLI client. The Replica Studio application
server and deployment materials are not published here.
