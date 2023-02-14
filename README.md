*This repository was created for the xontrib that xonsh [contains by default](https://github.com/xonsh/xonsh/tree/main/xontrib).* 

# xontrib-bashisms

Bash-like interface extensions for xonsh. Enables additional Bash-like syntax while at the command prompt.

For example:
```xsh
xontrib load bashisms
!!  # running the previous command
```

Note that these features are implemented as precommand events and
these additions do not affect the xonsh language when run as script.
That said, you might find them useful if you have strong muscle memory.

**Warning:** This xontrib may modify user command line input to implement its behavior.
To see the modifications as they are applied (in unified diffformat), please set ``$XONSH_DEBUG`` to ``2`` or higher.
The xontrib also adds commands: ``alias``, ``export``, ``unset``, ``set``, ``shopt``, ``complete``.
