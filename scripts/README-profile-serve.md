# profile-serve moved out of this fork

`scripts/profile_serve.py` was **private runtime glue** (the agent allowlist and
the kernel↔hermes launch design) and did not belong in this **public** fork.

It now lives in the private **AI-Dev-Workspace** repo at `hardline/profile_serve.py`
and is mounted into the hermes container via `/workspace`, launched as:

    /opt/hermes/.venv/bin/python3 /workspace/hardline/profile_serve.py

The `/fork` mount (this repo) is for hermes' own CLI source only.
