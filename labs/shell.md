### 1.1 Which shell am I using?

I am using Zsh on my Mac.

- Shell: Zsh
- Version: 5.9
- Command used: `echo $0` and `zsh --version`
### 1.2 Current working directory

I used the `pwd` command to check my current working directory.

My result was:

`/Users/muhammedsalihakpolat`

This is my personal home directory on macOS.

### 1.2 Where am I?

**Command 1:**
```bash
echo $HOME
```
**Output:**
```text
/Users/<user>
```

**Command 2:**
```bash
cd ~/Downloads && pwd
```
**Output:**
```text
/Users/<user>/Downloads
```

**Answer:** My home directory is `/Users/<user>`. My Downloads folder is located at `/Users/<user>/Downloads`.

### 1.3 Where do commands come from?

**Command:**
```bash
echo $PATH
```

**Output:** The PATH variable contains 12 directories.

**First directory searched:**
```text
/opt/anaconda3/bin
```

**Commands:**
```bash
which curl
which python3
which git
git --version
```

**Output:**
```text
/opt/anaconda3/bin/curl
/opt/anaconda3/bin/python3
/usr/bin/git
git version 2.50.1 (Apple Git-155)
```

**Answer:** My system searches for commands in 12 directories. The first directory is `/opt/anaconda3/bin`. Curl and Python3 are installed in Anaconda, while Git is located in `/usr/bin`.

### 1.4 How full is my disk?

**Command 1:**
```bash
df -h /
```

**Output:**
```text
Filesystem      Size  Used  Avail Capacity
/dev/disk3s1s1   228Gi 12Gi  89Gi  12%
```

**Command 2:**
```bash
du -sh ~/Downloads
```

**Output:**
```text
9.8G    /Users/<user>/Downloads
```

**Answer:** My disk has a total capacity of 228 GB, with 89 GB available. It is currently 12% full. My Downloads folder uses 9.8 GB of storage.

### 1.5 Stop a runaway process

**Command 1 (Terminal 1):**
```bash
sleep 600
```

**Command 2 (Terminal 2):**
```bash
ps aux | grep sleep
```

**Output:**
```text
PID 46124  grep sleep
PID 46122  sleep 600
```

**Command 3:**
```bash
kill 46122
```

**Output in Terminal 1:**
```text
zsh: terminated  sleep 600
```

**Answer:** The `sleep 600` process was running with PID 46122. I found it using `ps aux | grep sleep` and stopped it with the `kill` command. Two processes appeared because `grep sleep` also matches its own command. After killing the process, the first terminal showed that `sleep 600` had been terminated.

