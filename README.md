# InformationExperiment2

# ローカル環境に本リポジトリをクローンする手順

```powershell
cd "C:\任意のフォルダ"
git clone https://github.com/BP24043/InformationExperiment2
```


# GitHubのリモートリポジトリに接続する手順（※Windows）

## 1. ローカルリポジトリの作成
PowerShellで対象フォルダに移動し、以下を実行する。

```powershell
cd "C:\任意のフォルダ"
git init
git add .
git commit -m "Initial commit"
```

## 2. リモートリポジトリへの接続

GitHubのリポジトリページからURLを取得し、以下を実行する。

```powershell
git remote add origin https://github.com/アカウント名/リポジトリ名.git
git branch -M main
git push -u origin main
```

## 3. 2回目以降の更新

```powershell
git add .
git commit -m "変更内容"
git push
```

作業開始時には、他の人の変更を取り込むために以下を実行する。

```powershell
git pull origin main
```



# ファイルの追加・更新手順（GitHub）

## 1. 最新の変更を取得する

```powershell
git pull origin main
```

## 2. ファイルを追加・更新する

エディタなどでファイルを追加・編集する。

## 3. 変更内容を確認する

```powershell
git status
git diff
```

## 4. 変更をコミット対象に登録する

すべての変更を登録する場合：

```powershell
git add .
```

特定のファイルだけ登録する場合：

```powershell
git add ファイル名
```

## 5. 変更をコミットする

```powershell
git commit -m "変更内容の説明"
```

例：

```powershell
git commit -m "プレイヤーの移動処理を修正"
```

## 6. GitHubに変更を反映する

```powershell
git push
```

## 手順まとめ

```powershell
git pull origin main
git status
git add .
git commit -m "変更内容"
git push
```

## 注意事項
- `git add .` は不要なファイルや機密情報も登録する可能性があるため、実行前に確認する。
- `git pull` で競合が発生した場合は、競合を解決してからコミットする。
- `git push` が拒否された場合は、エラーメッセージを確認して対処する。


