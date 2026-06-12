# File System Simulator

A command line file system simulator written in Java. It mimics basic Unix-like commands using a tree structure built from scratch with custom data structures.

---

## Commands

| Command | Description |
|---------|-------------|
| `mkdir <name>` | Create a directory |
| `mkdir -p <path>` | Create nested directories |
| `cd <path>` | Change directory |
| `ls` | List contents of current directory |
| `pwd` | Print current path |
| `touch <file> <size>` | Create a file with a given size |
| `echo "text" > <file>` | Write text to a file |
| `grep "pattern" <file>` | Search for a pattern inside a file |
| `rm <name>` | Remove a file |
| `rm -r <name>` | Remove a directory recursively |
| `du` | Show total size of current directory |
| `tree` | Display directory tree |
| `exit` | Exit the program |

---

## Structure

| File | Description |
|------|-------------|
| `Main.java` | Entry point, reads and dispatches commands |
| `FileSystem.java` | Core logic for all commands |
| `Directory.java` | Directory node (HashMap + ArrayList for ordered children) |
| `FileNode.java` | File node with content and size |
| `Node.java` | Abstract base class for files and directories |
| `KMP.java` | KMP string search algorithm (used by `grep`) |
| `myStack.java` | Generic stack (used by `pwd`) |

---

## How to Run

```bash
javac *.java
java Main
```

---

## Notes

- `grep` uses the **KMP algorithm** for pattern matching
- `pwd` uses a custom **stack** to build the path from root
- Directories store children in insertion order for consistent `ls` and `tree` output
