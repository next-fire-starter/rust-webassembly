## Rustバージョン確認

```
cargo --version
rustc -V
rustup -V
rustup show
```

## インストール作業

### Rust で WebAssemblyを構築するためのツール

```
cargo install wasm-pack
```

### テンプレートプロジェクトを生成してくれる便利ツール(1度だけ)

```
cargo install cargo-generate
```

### プロジェクトを生成(1度だけ)

```
cargo generate --git https://github.com/rustwasm/wasm-pack-template --name myproject
cd /workspace/rust-webassembly/myproject
```

### コンパイル

```
cd /workspace/rust-webassembly/myproject
wasm-pack build
```

### Webプロジェクトを生成

```
cd /workspace/rust-webassembly/myproject
npm init wasm-app www
```
index.jsを編集


### 依存パッケージをインストール
```
cd /workspace/rust-webassembly/myproject/www
npm install
```

### ローカルのパッケージリンク

```
cd /workspace/rust-webassembly/myproject/pkg
npm link

cd /workspace/rust-webassembly/myproject/www
npm link myproject
```

## 実行

```
cd /workspace/rust-webassembly/myproject/www
npm run start
```
