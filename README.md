# Aura disposable live proof

Synthetic greeting example used only to exercise Aura's live build, tests,
independent validation, pull request, merge, and authoritative confirmation.

`greeting.py` provides `greet(name)`, which returns a greeting such as
`"Hi, Ada."`, and `multiply(a, b)`, which returns the product of its arguments.
For example, `multiply(3, 4)` returns `12`, `multiply(-3, 4)` returns `-12`,
`multiply(-3, -4)` returns `12`, and `multiply(0, 9)` returns `0`.

The initial recovery commissioning seed adds `subtract(a, b)` returning
`abs(a - b)`: `subtract(4, 3)` returns `1` and `subtract(0, 0)` returns `0`.
This intentionally seeded implementation has a known signed-result defect:
`subtract(3, 4)` returns `1` instead of `-1`, and `subtract(-3, 4)` returns `7`
instead of `-7`. It must be rejected by Aura's signed-subtraction acceptance
check and must not be accepted or merged. Only Aura's targeted REPAIR phase
may replace it with signed `a - b` and add negative-result tests.

Run the unittest suite in PowerShell with the configured Python executable:

```powershell
& 'C:/Users/nrsan/.codex/worktrees/aura-adaptive-v1/Aura/.venv/Scripts/python.exe' -B -m unittest -v
```
