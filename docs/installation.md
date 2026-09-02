# 導入・更新・削除

現在は初回ベータ版の公開準備中です。配布開始後は、以下の手順で導入できます。

## 必要なもの

- Windows版（Steam）Survival Log
- Release Noteに記載された対応ゲーム版
- BepInEx 6 `6.0.0-be.785+6abdba4`（Unity IL2CPP / Windows x64版）

BepInEx本体は日本語化MODのZIPに含まれません。先に[BepInExのReleases](https://github.com/BepInEx/BepInEx/releases)から`BepInEx-Unity.IL2CPP-win-x64-6.0.0-be.785+6abdba4.zip`を導入してください。

## BepInExを導入する

1. BepInExのZIPを展開します。
2. 中身を『Survival Log』のインストール先へコピーします。
3. ゲームを一度起動し、BepInExのコンソール画面が開いたらゲームを終了します。

## ゲームのインストール先を確認する

Steamで『Survival Log』を右クリックし、`管理` → `ローカルファイルを閲覧`を選びます。開いたフォルダーのパスを、以下のコマンドの`-GameRoot`へ指定します。

例:

```text
D:\SteamLibrary\steamapps\common\Survival Log
```

## 初めて導入する

1. [GitHub Releases](https://github.com/DainagonEl/survival-log-japanese/releases)からZIPをダウンロードして展開します。
2. ゲームを終了します。BepInExのコンソール画面も閉じてください。
3. 展開したフォルダーでPowerShellを開きます。
4. まず事前確認を実行します。ここではゲームファイルを変更しません。

```powershell
powershell.exe -NoProfile -ExecutionPolicy Bypass -File .\Install-SurvivalLogJapanese.ps1 `
  -GameRoot "D:\SteamLibrary\steamapps\common\Survival Log" `
  -Mode Preflight
```

5. エラーがなければ導入します。

```powershell
powershell.exe -NoProfile -ExecutionPolicy Bypass -File .\Install-SurvivalLogJapanese.ps1 `
  -GameRoot "D:\SteamLibrary\steamapps\common\Survival Log" `
  -Mode Install -Apply
```

## 新しい版へ更新する

新しいZIPを展開し、ゲームを終了してから実行します。

```powershell
powershell.exe -NoProfile -ExecutionPolicy Bypass -File .\Install-SurvivalLogJapanese.ps1 `
  -GameRoot "D:\SteamLibrary\steamapps\common\Survival Log" `
  -Mode Update -Apply
```

## 削除して元に戻す

導入時と同じZIPを使い、ゲームを終了してから実行します。

```powershell
powershell.exe -NoProfile -ExecutionPolicy Bypass -File .\Install-SurvivalLogJapanese.ps1 `
  -GameRoot "D:\SteamLibrary\steamapps\common\Survival Log" `
  -Mode Restore -Apply
```

導入前のファイルは`%LOCALAPPDATA%\SurvivalLogJapanese`に保存されます。このフォルダーは、元に戻すまで削除しないでください。

## 安全機能

インストーラーはゲーム版とファイルの状態を確認します。対応外の版、ゲーム起動中、導入後に対象ファイルが変わっている場合は、変更せずに停止します。エラーを無視して手作業で上書きしないでください。
