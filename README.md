## Building from source

**Prerequisites:** Rust (stable), Node.js 20+, platform system deps

Verify before cloning:
- `rustc --version` — 1.77+ 
- `node --version` — 20+

```sh
# macOS — no extra deps needed
# Linux
sudo apt-get install libwebkit2gtk-4.1-dev libssl-dev libayatana-appindicator3-dev librsvg2-dev

**Clone and run**
git clone https://github.com/mugiwaraluffy56/nova-editor.git
cd nova-editor
npm ci
npm run tauri dev
```

To produce a release build:

```sh
npm run tauri build
```

For a macOS universal binary:

```sh
rustup target add aarch64-apple-darwin x86_64-apple-darwin
npm run tauri build -- --target universal-apple-darwin
```
