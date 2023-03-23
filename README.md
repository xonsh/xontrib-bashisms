<p align="center">
Bash-like interactive mode extensions for the xonsh shell.
</p>

<p align="center">
If you like the idea click ⭐ on the repo and <a href="https://twitter.com/intent/tweet?text=Nice%20xontrib%20for%20the%20xonsh%20shell!&url=https://github.com/xonsh/xontrib-bashisms" target="_blank">tweet</a>.
</p>

## Note

We're not recommend to use this xontrib (see issues section). Use it carefully only if you have very strong muscle memory after hundred of years using Bash or for the education reasons and demonstration how agile is xonsh shell.

## Installation

To install use pip:

```bash
xpip install xontrib-bashisms
# or: xpip install -U git+https://github.com/xonsh/xontrib-bashisms
```

## Usage
```bash
xontrib load bashisms
```

Enables additional limited Bash-like syntax and commands while at the interactive command prompt:

| Added  | Meaning  |
|---|---|
| `!!`  | Get the last command.  |
| `!^`  | Get the first argument from the preceding command.  |
| `!$`  | Get the last argument from the preceding command.  |
| `!*`  | Get all argument from the preceding command.  |
| `alias`  | Add alias.  |
| `export NAME=Peter`  | Setting an environment variable.  |
| `shopt -s dotglob`  | Globbing files with * or ** will also match dotfiles, or those "hidden" files.  |
| `complete`  | Show list of completers.  |
| `set <-e/+e>`  |  Cause a failure after a non-zero return code.  |
| `set <-x/+x>` | Turns on tracing of source code lines during execution. |
| `unset NAME`  | Unsetting/deleting an environment variable.  |

See also [Bash to Xonsh Translation Guide](https://xon.sh/bash_to_xsh.html).

## Known issues

The `xontrib-bashisms` appeared in the beginning of xonsh history as part of the default xontribs. It has issues and we recommend to use [xontrib-sh](https://github.com/anki-code/xontrib-sh) instead.

### Threading issues

Because of xontrib-bashisms sets [`THREAD_SUBPROCS=False`](https://xon.sh/envvars.html#thread-subprocs) there are issues around the threading could appear. If you're using bashisms and faced with issues try the same in `xonsh --no-rc` mode before reporting the issue.

### Only interactive mode

The xontrib features are implemented as [on_precommand events](https://xon.sh/events.html#on-precommand) and
these additions do not affect the xonsh language when run as script.
That said, you might find them useful if you have strong muscle memory in interactive mode.

## Debug

This xontrib may modify user command line input to implement its behavior.
To see the modifications as they are applied (in unified diffformat), please set [`$XONSH_DEBUG`](https://xon.sh/envvars.html#xonsh-debug) to `2` or higher.

## See also

* [Bash to Xonsh Translation Guide](https://xon.sh/bash_to_xsh.html)
* [xontrib-sh](https://github.com/anki-code/xontrib-sh) - Paste and run commands from bash, zsh, fish, tcsh in xonsh shell.

## Credits

This package was created with [xontrib template](https://github.com/xonsh/xontrib-template).
