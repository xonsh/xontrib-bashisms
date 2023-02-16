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

Enables additional Bash-like syntax while at the command prompt.
For example, the ``!!`` syntax for running the previous command is now usable.

Note that these features are implemented as precommand events and
these additions do not affect the xonsh language when run as script.
That said, you might find them useful if you have strong muscle memory.

The xontrib also adds commands: ``alias``, ``export``, ``unset``, ``set``, ``shopt``, ``complete``.

## Known issues

This xontrib may modify user command line input to implement its behavior.
To see the modifications as they are applied (in unified diffformat), please set ``$XONSH_DEBUG`` to ``2`` or higher.

## Credits

This package was created with [xontrib template](https://github.com/xonsh/xontrib-template).
