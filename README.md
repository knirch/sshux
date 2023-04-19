# sshux
Wrap SSH sessions in tmux

## usage

sshux runs on the target system to which you have long running sessions. You
know the ones, the one your collegue or friend smugly told you "you should have
started screen or tmux" when you curse up a storm about losing work due to a
network outage.

Add sshux to your .bashrc on the server;

    /path/to/sshux-wrap && exit

The `&& exit` is needed to leave the shell when you disconnect from/ or end a
sshux session.

Now connect to your system and it should look just like normal. That's it.

If you connect to the system, sshux will attach to the first detached session
in the sshux namespace, or create a new session.

sshux aims to be as unintrusive as possible, the tmux configuration aims to be
as bare and non intrusive as possible. There's no prefix key, no status bars or
anything. Use `tmux` in your shell to modify the current session if needed.

If needed, consider a wrapper to make normal tmux operations less fiddly. See
example in `extras/tmux`.
