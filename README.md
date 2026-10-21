# InformationExperiment2



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