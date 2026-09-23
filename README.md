# RepInsight 公開Webページ

GitHub Pagesで `https://repinsight.jp` へ公開するための静的サイトです。JavaScript、Cookie、アクセス解析タグおよび外部Webフォントは使いません。

## 公開前に必ず行うこと

1. 法務ページ末尾の運営者名が `Rikuto Nakayama` で統一されていることを確認する。
2. `support@repinsight.jp` と `privacy@repinsight.jp` の送受信を確認する。
3. 各HTMLが `index,follow` で公開されていることを確認する。
4. 各ページに「公開前ドラフト」表示が残っていないことを確認する。
5. プライバシーポリシーの制定日と利用規約の施行日が `2026年9月24日` であることを確認する。
6. アプリの実際の通信先、収集データおよびApp Store Connectの申告と一致することを確認する。
7. 法的な最終判断が必要な場合は、日本法の専門家に確認する。

## GitHub Pagesの公開手順

1. GitHubに公開リポジトリ`repinsight-site`を作成する。
2. `website/`の中身をリポジトリ直下へ配置し、`main`ブランチのルートをGitHub Pagesの公開元にする。
3. GitHubのPages設定で、カスタムドメインに`repinsight.jp`を登録する。DNSより先にGitHub側へ登録する。
4. GitHubアカウントのPages設定から`repinsight.jp`を検証し、表示されたTXTレコードをDNSへ追加する。
5. お名前.comのDNSへ次のWeb用レコードを追加する。既存のMX、メールサーバー用A、SPF、DKIMおよびDMARCは変更・削除しない。

| 種別 | ホスト名 | 値 |
| --- | --- | --- |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `<GitHubユーザー名>.github.io` |

6. DNS反映後、`https://repinsight.jp/`と`https://www.repinsight.jp/`を確認し、GitHub Pagesで`Enforce HTTPS`を有効にする。
7. `support@repinsight.jp`への送受信を再確認し、Web用DNS追加によってメールが影響を受けていないことを確認する。

GitHubはapexドメインに4つのAレコードを指定し、`www`をGitHub Pagesの既定ドメインへ向ける構成を案内している。ワイルドカードDNSは使用しない。

## ページ

- `/`: 案内
- `/privacy/`: プライバシーポリシー
- `/terms/`: 利用規約
- `/support/`: サポート

## 法人化したとき

運営者名、連絡先、制定日・改定日を更新し、プライバシーポリシーと利用規約の改定履歴を残します。利用規約には事業承継条項を含めています。
