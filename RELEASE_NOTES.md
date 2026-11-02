# Replica Studio CLI 0.10.6

Standalone CLI release from Replica Studio `v0.10.6`.

## Asset

- `replica_cli.py`
- `replica_cli.py.sha256`

## Requirements

- Python 3.11+
- `requests>=2.32,<3`

```bash
python3 -m pip install "requests>=2.32,<3"
python3 replica_cli.py --help
```

The CLI supports device login, project/task inspection, upload, paid workflow
actions with explicit confirmation, waiting, download, and project deletion with
the corresponding token scopes.

The application server is not included in this repository or release.
