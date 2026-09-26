# Nape firmware

`main`はNapeの従来版とZMK Studio対応版をビルドします。`config/west.yml`でZMKとドライバーのコミットを固定しています。GitHub Actionsの成果物には`nape.uf2`と`nape-studio.uf2`が入ります。

Nape Consoleを使う場合は、別の[`console-beta`ブランチ](https://github.com/menbou0202/zmk-config-nape/tree/console-beta)から`nape-console.uf2`をビルドするか、そのβリリースから入手してください。Console版は専用のZMK forkとドライバーを使用します。

## 過去の利用者向け

旧ZMK向けの[`basic-driver`ブランチ](https://github.com/menbou0202/zmk-config-nape/tree/basic-driver)は、トラックボールの向きを実行時に切り替えるNape独自の処理を使わず、`inorichi/zmk-pmw3610-driver`を参照する保存版です。過去の利用者のため残していますが、新規利用には推奨しません。

別の旧ドライバーである[`menbou0202/zmk-pmw3610-driver`](https://github.com/menbou0202/zmk-pmw3610-driver)も過去の設定・forkの参照先として残しています。現在の`main`と`console-beta`はどちらも[`zmk-pmw3610-driver-nape`](https://github.com/menbou0202/zmk-pmw3610-driver-nape)を使用します。
