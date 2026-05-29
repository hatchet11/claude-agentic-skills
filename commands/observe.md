---
description: Agentic OS — cost dashboard + visual Command Center
argument-hint: [today|all|YYYY-MM-DD|center|visual]
---

Run the Agentic OS observability layer.

- If `$ARGUMENTS` is `center` (or `cc`): build and open the full visual **Command Center**
  (Overview, Cost, Infrastructure, Projects, Keys, Risks):
  ```
  python3 ~/agentic-os/observe/command_center.py --open
  ```
- If `$ARGUMENTS` is `visual`: build and open the visual **cost dashboard**:
  ```
  python3 ~/agentic-os/observe/build_dashboard.py --open
  ```
- Otherwise (empty, `today`, `all`, or a date): print the terminal cost dashboard:
  ```
  python3 ~/agentic-os/observe/dashboard.py $ARGUMENTS
  ```
  Default to `today` if `$ARGUMENTS` is empty. Print the output verbatim — do not summarize.
