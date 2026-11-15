# Reverse Engineering — Cheatsheet

## Static
- `file`, `strings`, `xxd`, `readelf -a`, `objdump -d`
- `checksec` — mitigations (NX, PIE, canary)
- Ghidra: import, auto-analyze, find main, Decompile window

## Dynamic
- `gdb ./prog` then `break *main`, `run`, `ni`, `si`, `x/s $rax`, `info registers`
- `strace` / `ltrace` — syscalls / libc calls

## Patching
- Find the compare/branch; flip with `set $eflags` or patch bytes

## Common tricks
- `strings | grep -i flag` first
- Look for `strcmp`/`memcmp` and the success branch

## Resources
- crackmes.one (practice), pwn.college (pwn progression)
