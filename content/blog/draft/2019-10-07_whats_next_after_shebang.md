+++
title = "What's next after shebang?"
date = 2019-10-07
draft = true
+++

## `set -e`

Makes sure the script exists on every error.

## `set -o pipefail`



## `set -x`

Sets verbose output

## Complete example

You can combine the `-e` and the `-o pipefail` command `set -eo pipefail` is equivalent.

```bash
#!/usr/bin/env bash

# Make sure that any errors cause the script to exit immediately.
set -eo pipefail
# Additional sets verbose output (traces) if the TRACE environment variable is
# set, e.g. `set TRACE=1`.
[[ "$TRACE" ]] && set -x
```
