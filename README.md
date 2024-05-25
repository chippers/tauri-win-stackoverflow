# Tauri + React + Typescript Stack Overflow Reproduction (Win11)

To reproduce, 

```bash
pnpm i
pnpm tauri dev
```

It's very unstable, sometimes it runs, sometimes it doesn't.

For me, the current version gives `thread 'main' has overflowed its stack`.

This only happens to me on Windows.

But if I remove a few unused crates from `Cargo.toml` or remove some capabilities, it will run.

If you run frontend and rust separately with release mode. It runs.

```bash
pnpm dev # start frontend dev server

# in another terminal
cd src-tauri
cargo run # this still gives stack overflow error
cargo run --release # this will run
```
