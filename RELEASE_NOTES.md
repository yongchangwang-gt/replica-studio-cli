# Replica Studio CLI 0.12.0

Standalone CLI exported from the Replica Studio `v0.12.0` source tag.

## What's Changed Since 0.10.6

- Added `portrait` to set a character portrait from a local image, the character
  library, or the character's history.
- Added `styles` and `style` to inspect and change art styles, including custom
  style descriptions and project-wide updates.
- `show` now includes cast identifiers, current portraits, style selection, and
  review findings for scripted workflows.
- `upload` now uploads without starting paid analysis by default. Use
  `--analyze --yes` to opt in; `--no-analyze` remains supported for compatibility.
- Paid actions still require the appropriate token scope and explicit `--yes`.
  Server-side rate or usage limits may still apply.

## Assets

- `replica_cli.py`
- `replica_cli.py.sha256`

## Requirements

- Python 3.11+
- `requests>=2.32,<3`

## Download And Verify

```bash
VERSION=0.12.0
BASE="https://github.com/yongchangwang-gt/replica-studio-cli/releases/download/v${VERSION}"

curl -fLO "$BASE/replica_cli.py"
curl -fLO "$BASE/replica_cli.py.sha256"
sha256sum -c replica_cli.py.sha256
```

On macOS:

```bash
shasum -a 256 -c replica_cli.py.sha256
```

The expected SHA-256 for `replica_cli.py` is:

```text
4e79376e1cd4b1eb2af988f021c8f99345a60d1c0d715eb2c5529a98618e0a81
```

## Run

```bash
python3 -m pip install "requests>=2.32,<3"
python3 replica_cli.py --help
python3 replica_cli.py login --label "My computer"
```

The Replica Studio application server and deployment materials are not included
in this repository or release.
