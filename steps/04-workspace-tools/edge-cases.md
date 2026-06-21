# Edge cases — Этап 4

## File System

- [ ] File changed between read and write → **stale hash** reject
- [ ] **Path traversal** outside workspace
- [ ] Paths with spaces, Unicode, Windows vs POSIX separators
- [ ] Symlink escapes workspace
- [ ] File too large for context
- [ ] Non-UTF-8 encoding
- [ ] Patch stale context

## Shell

- [ ] Command runs **indefinitely** → timeout + kill
- [ ] Dev server / watcher → background or deny
- [ ] Interactive stdin / TTY required
- [ ] Non-zero exit vs zero exit with errors
- [ ] **Huge stdout/stderr** → max output
- [ ] Wrong **working directory**
- [ ] Child processes outlive parent

## Security (basics)

- [ ] Path traversal
- [ ] Secrets in command args or logs

→ [Этап 3](../03-tool-runtime/edge-cases.md) · [Этап 5](../05-coding-cli/edge-cases.md)
