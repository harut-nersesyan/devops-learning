
# Linux Process Management

## View Running Processes

- `ps aux` - Show all running processes.
- `top` - Monitor processes in real time.
- `ps aux | head` - Show the first processes in the list.

## Find Processes

- `pgrep -fl sleep` - Find processes matching the name sleep.
- `ps -p PID -o pid,ppid,%cpu,%mem,comm` - Show information about a specific process.

## Background Processes

- `sleep 500 &` - Start a process in the background.
- `&` - Run a command in the background.

## Kill Processes

- `kill PID` - Send a termination signal to a process.
- `kill -9 PID` - Forcefully terminate a process (use only when necessary).

## Practical Example

Start a background process:

```bash
sleep 500 &
```

Find its PID:

```bash
pgrep -fl sleep
```

Terminate the process:

```bash
kill PID
```

Verify that the process has stopped:

```bash
pgrep -fl sleep
```

If there is no output, the process is no longer running.

