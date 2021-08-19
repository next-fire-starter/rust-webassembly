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
cd myproject
```

### コンパイル

```
cd myproject
wasm-pack build
```

### Webプロジェクトを生成

```
cd myproject
npm init wasm-app www
```
index.jsを編集


### 依存パッケージをインストール
```
cd myproject/www
npm install
```

### ローカルのパッケージリンク

```
cd myproject/pkg
npm link

cd myproject/www
npm link myproject
```

## 実行

```
cd myproject/www
npm run start
```
