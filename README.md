# Nape firmware

`main`はNape Console正式版に対応した`nape-console.uf2`をビルドします。`console-beta`の変更は`main`へ統合済みです。`config/west.yml`で専用ZMK forkとドライバーのコミットを固定しています。

## ファームウェアを使う

[最新Release](https://github.com/menbou0202/zmk-config-nape/releases/latest)の「Assets」から`nape-console.uf2`をダウンロードしてください。ビルド済みファームウェアの利用にGitHubアカウントやForkは不要です。

- [ファームウェアの書き込み方法](https://github.com/menbou0202/Nape/blob/main/doc/build-guide.md)
- [Nape Consoleの使い方](https://github.com/menbou0202/nape-console/blob/main/HOW_TO_USE.md)
- [Nape Consoleを開く](https://menbou0202.github.io/nape-console/)

## 自分のForkでビルドする場合

1. GitHubにログインし、このリポジトリ右上の「Fork」から自分のアカウントへコピーします。
2. 自分のForkで「Actions」を開き、有効化の確認が表示されたらワークフローを有効にします。
3. `main`の`config/nape.keymap`などを編集し、コミット・pushするとビルドが始まります。
4. 変更せずにビルドする場合は、「Actions」→「Build ZMK firmware」→「Run workflow」で`main`を選びます。
5. 成功した実行結果の「Artifacts」から`firmware`のZIPをダウンロードし、展開して`nape-console.uf2`を取り出します。

以前からのForkを同期する場合、現在の`main`では従来版ではなくNape Console対応ファームウェアがビルドされる点に注意してください。

## 過去の利用者向け

旧ZMK向けの[`basic-driver`ブランチ](https://github.com/menbou0202/zmk-config-nape/tree/basic-driver)は、トラックボールの向きを実行時に切り替えるNape独自の処理を使わず、`inorichi/zmk-pmw3610-driver`を参照する保存版です。過去の利用者のため残していますが、新規利用には推奨しません。

別の旧ドライバーである[`menbou0202/zmk-pmw3610-driver`](https://github.com/menbou0202/zmk-pmw3610-driver)も過去の設定・forkの参照先として残しています。現在の`main`は[`zmk-pmw3610-driver-nape`](https://github.com/menbou0202/zmk-pmw3610-driver-nape)を使用します。
