# Aura disposable live proof

Synthetic greeting example used only to exercise Aura's live build, tests,
independent validation, pull request, merge, and authoritative confirmation.

`greeting.py` provides `greet(name)`, which returns a greeting such as
`"Hi, Ada."`, and `multiply(a, b)`, which returns the product of its arguments.
For example, `multiply(3, 4)` returns `12`, `multiply(-3, 4)` returns `-12`,
`multiply(-3, -4)` returns `12`, and `multiply(0, 9)` returns `0`.

`subtract(a, b)` returns the signed difference `a - b`. For example,
`subtract(4, 3)` returns `1`, `subtract(3, 4)` returns `-1`,
`subtract(-3, 4)` returns `-7`, and `subtract(0, 0)` returns `0`.
The targeted recovery repair replaces the initial `abs(a - b)` seed and adds
tests for negative results.

Run the unittest suite in PowerShell with the configured Python executable:

```powershell
& 'C:/Users/nrsan/.codex/worktrees/aura-adaptive-v1/Aura/.venv/Scripts/python.exe' -B -m unittest -v
```
