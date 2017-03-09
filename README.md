# plop

plop is a Bash script for GNU/Linux systems that daemonizes any program given as argument while permitting to keep control over it.

plop consists of a single shell script. Managed processes (for a given user) are identified by their basename. PID and PGID are stored in files in $XDG_RUNTIME_DIR (or /tmp if undefined).

Current possible actions are:

 - start: Daemonize the program provided as argument (relative or absolute filename).
 - stop: Stop the daemon (by name)
 - status: Show daemon process(es) (by name)
 - attach: Attach stdout and stderr of the current terminal to file descriptors 1 and 2 of the daemon
 - detach: Close file descriptors 0, 1 and 2 of the daemon

The file _example_ provide a minimal… example… of a executable that can be run by plop. As you can see, there is no specific need and plop should be able to run any executable without modification. Programs run by plop don’t need to fork by themselves (and probably shouldn’t…).
