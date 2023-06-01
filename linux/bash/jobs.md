## background jobs

Using the Job Control of bash to send the process into the background:
```
1. Ctrl+Z to stop (pause) the program and get back to the shell.
2. bg to run it in the background.
3. disown -h [job-spec] where [job-spec] is the job number (like %1 for the first running job; find about your number with the jobs command) so that the job isn't killed when the terminal closes.
```
