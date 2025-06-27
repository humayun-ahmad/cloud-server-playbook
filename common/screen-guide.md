# Screen Command Complete Guide

A comprehensive guide to using GNU Screen for managing terminal sessions that persist even after disconnecting from SSH or closing terminal windows.

## What is Screen?

Screen is a terminal multiplexer that allows you to create, manage, and navigate between multiple terminal sessions. It's particularly useful for:
- Running long processes that shouldn't be interrupted
- Maintaining sessions across SSH disconnections
- Managing multiple terminal windows in a single session

## Installation

### Ubuntu/Debian
```bash
sudo apt update
sudo apt install screen
```

## Basic Usage

### Starting a Screen Session

#### Start a new session
```bash
screen
```
*Press Enter when you see the welcome message to access your shell.*

#### Start a named session (recommended)
```bash
screen -S session_name
```

**Example:**
```bash
screen -S my_python_script
```

### Session Management

#### Detach from current session
Keep the session running in the background:
```
Ctrl + A, then D
```

#### List all active sessions
```bash
screen -ls
```

**Example output:**
```
There is a screen on:
    1234.my_python_script    (Detached)
1 Socket in /run/screen/S-yourusername.
```

#### Reattach to a session
By session name:
```bash
screen -r session_name
```

By session ID:
```bash
screen -r 1234
```

**Example:**
```bash
screen -r my_python_script
```

### Session Information

#### Get current screen session name
While inside a screen session:
```bash
echo $STY
```

**Output:**
```
12345.my_session_name
```

## Terminating Sessions

### Exit from inside a session

#### Method 1: Type exit
```bash
exit
```

#### Method 2: Keyboard shortcut
```
Ctrl + D
```

#### Method 3: Quit command
```
Ctrl + A, then type :quit
```

#### Method 4: Kill shortcut
```
Ctrl + A → K → y
```

### Kill sessions externally

#### Kill by full session name
```bash
screen -S 12345.my_session_name -X quit
```

#### Kill by session name only
```bash
screen -S my_session_name -X quit
```

#### Kill all screen sessions
⚠️ **Warning: This terminates ALL screen sessions**
```bash
killall screen
```

## Advanced Usage

### Reattach to specific sessions
When multiple sessions exist:
```bash
screen -r 1234.screen1
```

Or using partial name matching:
```bash
screen -r screen1
```

## Common Use Cases

- **Long-running scripts**: Start your script in a screen session, detach, and let it run
- **SSH sessions**: Maintain your work environment even if connection drops
- **System monitoring**: Keep monitoring tools running continuously
- **Development**: Maintain multiple terminal environments for different projects

## Quick Reference

| Action | Command |
|--------|---------|
| Start new session | `screen` |
| Start named session | `screen -S name` |
| Detach | `Ctrl + A, D` |
| List sessions | `screen -ls` |
| Reattach | `screen -r name` |
| Kill session | `screen -S name -X quit` |
| Get current session | `echo $STY` |

## Tips

- Always use named sessions for better organization
- Use descriptive names that indicate the session's purpose
- Regularly clean up unused sessions to avoid clutter
- Remember that detached sessions continue running and consuming resources
