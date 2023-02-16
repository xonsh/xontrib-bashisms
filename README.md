<p align="center">
Bash-like interface extensions for xonsh.
</p>

<p align="center">  
If you like the idea click ⭐ on the repo and <a href="https://twitter.com/intent/tweet?text=Nice%20xontrib%20for%20the%20xonsh%20shell!&url=https://github.com/xonsh/xontrib-bashisms" target="_blank">tweet</a>.
</p>


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

* `!!`, `!$`, `!^`, `!*`
* `alias`
* `export`
* `unset`
* `set`
* `shopt`
* `complete`
* `set <-e|+e|-x|+x>`

## Known issues

Note that these features are implemented as [precommand events](https://xon.sh/events.html#on-precommand) and
these additions do not affect the xonsh language when run as script.
That said, you might find them useful if you have strong muscle memory.

This xontrib may modify user command line input to implement its behavior.
To see the modifications as they are applied (in unified diffformat), please set [`$XONSH_DEBUG`](https://xon.sh/envvars.html#xonsh-debug) to `2` or higher.

## See also

* [Bash to Xonsh Translation Guide](https://xon.sh/bash_to_xsh.html)
* [xontrib-sh](https://github.com/anki-code/xontrib-sh) - Paste and run commands from bash, zsh, fish, tcsh in xonsh shell. 

## Credits

This package was created with [xontrib template](https://github.com/xonsh/xontrib-template).
