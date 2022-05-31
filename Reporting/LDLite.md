| ソース | 取得日 |
| ---- | ---- |
| [Library Data Platform](https://github.com/folio-org/docs/tree/lotus/content/en/docs/Reporting/LDLite) | 2022-04-14 |

## LDLite

LDLiteは、図書館データプラットフォーム・プロジェクトの一部であるツールです。LDLiteは、LDPデータレポートサーバをインストールすることなく、LDPデータの基本的なレポート機能を提供します。また、LDPデータベースをFOLIOの追加データまたはリアルタイムデータで補完するために使用することができます。

LDLiteでは、ユーザーが直接FOLIOに問い合わせることができます。Okapiベースのサービスに接続すると、LDLiteソフトウェアは、JSON変換などLibrary Data Platformソフトウェア全体の機能の一部を提供することができます。変換されたデータは、ユーザーのコンピュータ上の単純なファイルとして組み込みデータベースに保存することも、LDPデータベースのような共有データベースに保存することも可能です。LDLiteをインストールするには、ユーザーがPythonを実行している必要があります。

LDLiteは、SRS（Source Record Storage）から取得したMARCデータのレポートにも利用することができます。この機能はまだ実験段階であり、現時点では正式にサポートされていません。LDLiteからMARCデータにアクセスするための設定方法は、[GitHub](https://github.com/library-data-platform/ldlite/blob/main/srs.md)で公開されています。

LDLiteの詳細とコードベースへのアクセスは、[GitHubリポジトリ](https://github.com/library-data-platform/ldlite)を参照してください。FOLIOのJuniperリリースとの互換性のために、ユーザーがLDLiteの特定のバージョンを必要とすることはありません。