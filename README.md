# executables

> A collection of useful shell scripts for macOS

## Prerequisites

- macOS
- gsed (GNU sed)

## Installation

### Clone the Repository

```sh
git clone https://github.com/chrisbradleydev/executables.git
cd executables
```

### Setup Script Symlinks

To make these scripts available system-wide, create symlinks in `/usr/local/bin`:

```sh
sudo ln -s "$(pwd)/bud" /usr/local/bin/bud
sudo ln -s "$(pwd)/google-chrome-hard-refresh" /usr/local/bin/google-chrome-hard-refresh
sudo ln -s "$(pwd)/stop" /usr/local/bin/stop
sudo ln -s "$(pwd)/zoom" /usr/local/bin/zoom
```

After installation, you can run any script from anywhere in your terminal.

## Scripts

### bud

Creates a tar.gz archive of the current directory and moves it to the archive directory.

**Usage:**

```sh
bud
```

**Features:**

- Archives the current directory using its name as the filename
- Excludes the archive file itself from being included
- Moves the archive to the archive directory

### google-chrome-hard-refresh

Performs a hard refresh (Cmd+Shift+R) on the active Google Chrome tab.

**Usage:**

```sh
google-chrome-hard-refresh
```

**Features:**

- Brings Google Chrome to the foreground
- Executes a hard refresh to bypass cache

### stop

Kills processes running on a specified TCP port.

**Usage:**

```sh
stop <port>
```

**Arguments:**

- `port` - The TCP port number

**Examples:**

```sh
stop 3000   # Kill process running on port 3000
stop 8080   # Kill process running on port 8080
```

**Features:**

- Finds processes using the specified port
- Force kills the process with SIGKILL

### zoom

Updates the zoom level in VS Code and Cursor settings across all profiles.

**Usage:**

```sh
zoom [level]
```

**Arguments:**

- `level` - Zoom level (default: 0). Can be positive or negative numbers, including decimals

**Examples:**

```sh
zoom 2      # Increase zoom to 2
zoom -0.5   # Decrease zoom to -0.5
zoom        # Reset zoom to 0
```

**Features:**

- Updates both VS Code and Cursor settings
- Handles all user profiles automatically
