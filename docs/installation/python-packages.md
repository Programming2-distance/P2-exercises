---
layout: page
---

# Installing Extra Packages

**IMPORTANT**

> A `$` in the beginning of a line means that you should input that line in a shell.
> Do not write the `$` itself though, only what follows.
> For example, `$ ls` means you should type `ls` followed by enter.

In the terminal, write

```bash
$ pip install pytest pytest-timeout mypy
```

## Checking

Open the terminal in the `00-setting-things-up` directory and enter (only the first line! The other lines are expected output)

```bash
$ pytest
..                               [100%]
2 passed in 0.01s
```

If you get the same output, you have successfully installed the Python packages.
Otherwise, ask a lecturer for help.
