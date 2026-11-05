# PDF書き込み君：Codex適用記録
確認日：2026-11-05（日本時間）。対象：ken-tak-steam/pdf_kakikomikun の取得時の既定ブランチ。アプリ本体の改修・実機テストは今回実施していない。

## 確認した現状
約1.37MBのHTMLをblob取得。外部script srcなし。ライセンス情報ボタンとGitHubリンクあり。通常保存の暗号化系エラー時にconfirmし、承認時だけflatten操作へ進むコードを確認。READMEでは追加テキストのみ画像化するため、追加文字は選択・検索できない。元文字の保持と区別する。

## 本体ライセンス
LICENSE.md、DISCLAIMER.mdとindex.html内の独自の非商用条件を確認。LICENSE.mdは実費・参加費徴収を商用と扱わないと記載。アプリ内は学校教育・講習会等を認める文面で、表現差がある。意味を勝手に統一せず対照表を作る。

## 依存ライブラリ・付属データ
READMEとLICENSE.mdにPDF.js 2.5.207（Apache-2.0）、pdf-lib 1.17.1（MIT）。HTML内のPDF.js Workerバージョン2.5.207、Apache通知を確認。第三者通知の全文・内蔵pdf-libと推移的依存の対応は追加確認が必要。THIRD_PARTY_NOTICES.txtは取得404。

## 次の適用順序
優先1：通常PDFの元文字・リンク保持、暗号化時の承認/キャンセル、別名保存を実物PDFで確認。優先2：README・ライセンス表示の相違を整理。優先3：追加文字の検索可能性を改善する場合はフォント埋込みとライセンス・容量の調査から始める。既存機能を無断で全面画像化しない。

## 取得根拠
- README.md: 53d4dcdd26a303238e2f3c78deab3c1388989f6f
- LICENSE.md: e967618c7aeb6fa0febdf372b746172e3fe47f25
- index.html: 4998092ac38d25e5866ef71bd62ee381a46c106d
ソース：https://github.com/ken-tak-steam/pdf_kakikomikun
取得したコードとREADMEの記述、過去チャットの報告は区別する。取得時点のファイル単位のSHAであり、リポジトリ全体の同一コミットを保証しない。

## 今回の変更範囲
AGENTS.mdとdocs/CODEX_APP.md、docs/CODEX_TEMPLATES.mdの追加のみ。既存HTML・ライセンス本文・依存バージョン・公開設定は変更しない。共通ルールは目標であり、現アプリが全条件を満たす証明ではない。
