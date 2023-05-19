# 練習の手順
# 前準備
- node.jsのインストール
- npmのインストール(npmコマンドが実行できる)
## 実行環境を作る
### ディレクトリを作る
- $mkdir practiceを実行
- $cd practiceを実行
### ファイルを作る
- $npm init --yes(--yesは全ての質問をyesで答えデフォルト値とするオプション)を実行
- package.jsonが作成される
- package.jsonに変更を加える
- "module""の追加が必要

```
"main": "index.js",
```
↓  ↓  ↓

```
"main": "index.js",
"type": "module",
```

### TypeScriptをインストール
- $npm install --save-dev typescript @types/nodeを実行
- node_modulesディレクトリ, package-lock.jsonが作成される
- tsconfig.jsonを作成する
- $npx tsc --initを実行
- tsconfig.jsonに変更を加える(必要に応じて)
- "target"の変更

```
"target": "es2016"
```
↓  ↓  ↓

```
"target": "ES2020"
```

- "module"の変更

```
"module": "commonjs",
```
↓  ↓  ↓

```
"module": "ESNEXT"
```

- moduleResolutionコンパイラオプションをnodeに

```
//"moduleResolution": "node",
```
↓  ↓  ↓

```
"moduleResolution": "node",
```

- "outDir"の変更

```
//"outDir": "./",
```
↓  ↓  ↓

```
"outDir": "./dist",
```

- 最後にincludeオプションを設定
```
{
 "compilerOptions": {
    //沢山のコンパイラオプション達
 },
// ↓ ここに追加する
 "include": ["./src/**/*.ts"]
}
```

### 初めてのTypeScriptプログラム
- srcディレクトリを作成
- srcディレクトリにindex.tsを作成
- index.tsにコードを記述
- プロジェクトに移動し$npx tscを実行
- distディレクトリが作成される
- distディレクトリにindex.jsが作成される
- $node dist/index.jsを実行(パスの位置に注意)
- 実行結果が表示される

[English](README_EN.md)