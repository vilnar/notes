## Kill process by name

```sh
ps -ef | grep '{process_name}' | grep -v grep | awk '{print $2}' | xargs -r kill
sudo ps -ef | grep '{process_name}' | grep -v grep | awk '{print $2}' | sudo xargs -r kill
sudo ps -ef | grep '{process_name}' | grep -v grep | awk '{print $2}'
```

## Find process by name

```sh
ps aux | grep 'firefox'
```


## find location process

```sh
pwdx {PID}
lsof -p {PID} | grep cwd
```


## kill

```sh
kill {PID}
```

if the previous command does not work
SIGTERM - негайнно завершує процес, але оброблюється програмою, тому дозволяє завершити дочірні процеси і звільнити всі ресурси;
```sh
kill -TERM {PID}
```

if the previous command does not work
SIGKILL - негайно завершує процес, але на відміну від попереднього, сигнал обробляється ядром. Тому ресурси і дочірні процеси залишаються запущеними.
```sh
kill -KILL {PID}
```

## run command in background

```
command > /dev/null 2>&1 &
```
`> /dev/null 2>&1` means redirect stdout to /dev/null and stderr to stdout .

Use the jobs utility to display the status of all stopped and background jobs in the current shell session:
```sh
jobs -l
```
To bring a background process to the foreground, use the fg command:
```sh
fg
```

## top filter few command

row top
```
PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND
```

command
```sh
top -bc | grep "vim\|emacs"
```
