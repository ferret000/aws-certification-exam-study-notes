# [DVA-C02]試験範囲内の AWS のサービスと機能<!-- omit in toc -->

## 1. はじめに

- [DVA-C02] AWS Certified Developer - Associate の試験範囲内の AWS サービスと機能についてまとめます
- 試験概要は[**こちら**](./DVA-C02_勉強記録.md)を参照してください
- 記載内容は、ChatGPT、AWS 公式ページ[^1]、Udemy 講座の解説[^2]、その他 Web サイト[^3][^4][^5][^6]を基にしています。
  - ChatGPT に概要を追加させたものを記載。勉強を進める中で更新予定。

## 2. 範囲内の AWS のサービスと機能

### 2.1. 分析

#### 2.1.1. Amazon Athena

##### 概要

- 標準 SQL を使用して Simple Storage Service (Amazon S3) 内のデータを直接、シンプルに分析できるようにするインタラクティブなクエリサービス。

#### 2.1.2. Amazon Kinesis

##### 概要

- ストリーミングデータをリアルタイムで収集、処理するためのサービス。データ分析やストリーム処理に利用される。

#### 2.1.3. Amazon Kinesis Data Streams

##### 概要

- 大量のストリーミングデータをリアルタイムに収集して、ETL 処理などを実施した上で、他の AWS サービスに送信することができるリアルタイムデータ処理用のサービス。
- 1 秒以下のデータロードが達成できる性能があり、ストリーミングデータをリアルタイムに処理したり、表示させたい場合に利用
- サーバーレスで動作。
- データ処理アプリケーション（Kinesis Data Streams アプリケーション）を作成して使用。
  - アプリケーションは Kinesis Client Library (KCL) を活用して構築可能。
  - 実行環境には Amazon EC2 インスタンス を使用。

#### 2.1.4. Amazon Kinesis Data Firehose

##### 概要

- 工場のデバイスから送信されるストリームデータを取得して保存するソリューション。
- Amazon Kinesis Data Firehose のレコード形式の変換を有効にすることで、Amazon S3 バケットに送信するレコード方式に変換することが出来るが、これはデータ変換までは実施しない。Firehose ストリーム用に設定できる送信先は Amazon S3 のみ。
- データロードまで 60 秒必要となるため、ミリ秒単位の処理には利用できないが、データを変換してストレージ（例: Amazon S3）などに配信する用途には向いている。
  - Kinesis Data Streams からデータを受け取って処理を継続可能。
  - Lambda 関数 を組み込んでデータ変換処理を実行可能。

#### 2.1.5. Amazon OpenSearch Service

##### 概要

- オープンソースの検索および分析エンジンである OpenSearch をマネージドで提供。ログ分析や検索エクスペリエンスに使用。
- Elasticsearch は今後サポートしない？

### 2.2. アプリケーション統合

#### 2.2.1. AWS AppSync

##### 概要

- GraphQL API を構築し、リアルタイムデータ同期と API 作成を容易にするサービス。

#### 2.2.2. Amazon EventBridge

##### 概要

- AWS サービスや独自アプリケーション間のイベントを接続・統合するための、サーバーレスなイベントバスサービス。
- アマゾン ウェブ サービスのリソースの変更を記述した、システムイベントのほぼリアルタイムのストリームを配信する。

##### 主な機能

##### 公式ページ

- [Amazon EventBridge とは](https://docs.aws.amazon.com/ja_jp/eventbridge/latest/userguide/eb-what-is.html)
- [Amazon EventBridge イベント](https://docs.aws.amazon.com/ja_jp/eventbridge/latest/userguide/eb-events.html)

#### 2.2.3. Amazon Simple Notification Service (Amazon SNS)

##### 概要

- メッセージ配信やアプリケーション通知を提供するパブリッシュ/サブスクライブ型メッセージングサービス。

#### 2.2.4. Amazon Simple Queue Service (Amazon SQS)

##### 概要

- 分散アプリケーション間での非同期メッセージ処理を簡単に実現するキューイングサービス。

#### 2.2.5. AWS Step Functions

##### 概要

- サーバーレスのワークフローオーケストレーションサービスで、複雑なプロセスを簡単に自動化。
- 複雑な分散アプリケーションのワークフローを簡単にオーケストレーションするための、サーバーレスなワークフローオーケストレーションサービス。

##### 主な機能

- タスク状態フィールド
  - Resource (必須)
  - Arguments (オプション、 JSONata のみ)
  - Output (オプション、 JSONata のみ)
  - Parameters (オプション、 JSONPath のみ)
  - Credentials (オプション)
  - ResultPath (オプション、 JSONPath のみ)
  - ResultSelector (オプション、 JSONPath のみ)
  - Retry (オプション)
    - 状態でランタイムエラーが発生した場合の再試行ポリシーを定義する。
    - 個々のステートレベルで設定
  - Catch (オプション)
  - TimeoutSeconds (オプション)
    - アクティビティまたはタスクが States.Timeout エラーでタイムアウトして失敗するまでに実行できる最大時間を指定する。
    - タイムアウトの値はゼロ以外の正の整数にする必要がある。
    - デフォルト値は 99999999 。
  - TimeoutSecondsPath (オプション、 JSONPath のみ)
  - HeartbeatSeconds (オプション)
    - タスクがハートビートシグナルを待機する最大間隔を定義する。
  - HeartbeatSecondsPath (オプション、 JSONPath のみ)
- API アクション
  - [CreateActivity](https://docs.aws.amazon.com/ja_jp/step-functions/latest/apireference/API_CreateActivity.html)
    - アクティビティの Amazon Resource Name (ARN) を取得する
  - [DeleteActivity](https://docs.aws.amazon.com/ja_jp/step-functions/latest/apireference/API_DeleteActivity.html)
    -
  - [GetActivityTask](https://docs.aws.amazon.com/ja_jp/step-functions/latest/apireference/API_GetActivityTask.html)
    - スケジュールされたタスクを取得する
  - [SendTaskHeartbeat](https://docs.aws.amazon.com/ja_jp/step-functions/latest/apireference/API_SendTaskHeartbeat.html)
    - タスクの進行状況を報告する
  - [SendTaskSuccess](https://docs.aws.amazon.com/ja_jp/step-functions/latest/apireference/API_SendTaskSuccess.html)
    - タスクの成功を報告する
  - [SendTaskFailure](https://docs.aws.amazon.com/ja_jp/step-functions/latest/apireference/API_SendTaskFailure.html)
    - タスクの失敗を報告する
  - [StartExecution](https://docs.aws.amazon.com/ja_jp/step-functions/latest/apireference/API_StartExecution.html)
    - ステートマシン全体を起動する
  - [StopExecution](https://docs.aws.amazon.com/ja_jp/step-functions/latest/apireference/API_StopExecution.html)
    - ステートマシン全体を停止する

##### 公式ページ

- [Task](https://docs.aws.amazon.com/ja_jp/step-functions/latest/dg/state-task.html)
- [Step Functions のエラー処理](https://docs.aws.amazon.com/ja_jp/step-functions/latest/dg/concepts-error-handling.html)
- [アクティビティタスクの完了を待機中](https://docs.aws.amazon.com/ja_jp/step-functions/latest/dg/concepts-activities.html#activities-wait)

### 2.3. コンピューティング

#### 2.3.1. Amazon EC2

##### 概要

- 仮想サーバーをプロビジョニングして、アプリケーションをホストできるクラウドインフラサービス。

##### 主な機能

- ユーザーデータ
  - Amazon EC2 インスタンスの起動設定時にユーザーデータを利用することで、インスタンス起動時にスクリプトを実行可能。
- ブートストラップ
  - インスタンスにユーザーデータを渡すことで、起動時に実行される処理。
- インスタンスタイプ
  - 汎用
    - A1、M5、T3 など
  - コンピューティング最適化
    - C5、C6g など
  - メモリ最適化
    - X1、R5、ハイメモリ、z1d など
    - メモリ内の大きいデータセットを処理するワークロードに対して高速なパフォーマンスを実現する
  - ストレージ最適化
    - H1、D2、I3、I3en など
  - 高速コンピューティング
    - P3、Inf1、G4（GPU）、F1（FPGA）など
- 購入方式
  - オンデマンドインスタンス
    - 通常のインスタンス購入方法
    - オンデマンドキャパシティー予約
      - コミットメントは不要
      - 特定の AZ のキャパシティを予約して利用可能
      - リージョン毎のオンデマンドインスタンス数に制限
  - リザーブドインスタンス
    - 1 年または 3 年の期間利用を予約することで最大 75％の割引
  - スケジュールドリザーブドインスタンス
    - 2021 年に利用停止となった為、代わりにオンデマンドキャパシティー予約をすることが推奨されている。
  - スポットインスタンス
    - 最大 90％の割引
    - 実行時間に柔軟性がある場合や、中断出来る処理に利用する。

#### 2.3.2. AWS Elastic Beanstalk

##### 概要

- Web アプリケーションやサービスのデプロイとスケーリングを簡素化する PaaS (Platform as a Service)。

#### 2.3.3. AWS Lambda

##### 概要

- サーバーレスでコードを実行するためのサービス。インフラストラクチャの管理不要で、イベント駆動型の処理が可能。
- 最大 10GB までのデータ容量を扱うことが可能。
  - 2022 年５月より、AWS Lambda のアップデートで最大 10GB まで拡張可能となったエフェメラルストレージを拡張できるようになった。
- SAA-C03 の試験ガイドでは `サーバーレス` に分類。

##### 主な機能

- バージョン
- エイリアス
  - すべてのエイリアスには独自の ARN がある。
    - したがって、新しいバージョンのエイリアスが発行されるときに、イベントソースマッピングを新しい ARN で更新する必要がありる。
  - Lambda エイリアスは別の Lambda エイリアスに割り当てることはできず、Lambda 関数のバージョンのみに割り当てることができる。
- レイヤー
  - 特定のバージョンの Lambda 関数を指すポインタ
- イベントソースマッピング

  - バージョン ARN またはエイリアス ARN に割り当てることができる。
    - イベントソースマッピングで Lambda 関数に ARN を使用する代わりに、エイリアス ARN を使用できる為、新しいバージョンの昇格時または以前のバージョンへのロールバック時にイベントソースマッピングを更新する必要がない。
  - レイヤー ARN には割り当てられない。

##### 公式ページ

- [Lambda 関数のバージョン](https://docs.aws.amazon.com/ja_jp/lambda/latest/dg/configuration-versions.html)
- [Lambda 関数のエイリアス](https://docs.aws.amazon.com/ja_jp/lambda/latest/dg/chapter-layers.html)
- [Lambda レイヤーの作成と共有](https://docs.aws.amazon.com/ja_jp/lambda/latest/dg/chapter-layers.html)
-

#### 2.3.4. AWS Serverless Application Model (AWS SAM)

##### 概要

- CloudFormation テンプレートと連携してサーバーレスアプリケーションをデプロイするためのツール。
- AWS SAM がアプリケーションをデプロイする際は CloudFormation と連携し、SAM が SAM 構文を AWS CloudFormation 構文に変換および拡張することで、CloudFormation テンプレートからサーバーレスアプリケーションの構築を実行する。
- サーバーレスアプリケーションをローカルで構築、テスト、およびデバッグするための環境をデプロイ可能。

  - オンプレミスの VMware vSphere、Microsoft Hyper-V/SCVMM、または Azure 仮想マシンを AWS 環境に移行する。

- サーバーレスアプリケーションの構築、デプロイ、テストのためのフレームワーク。
- SAA-C03 の試験ガイドでは `マネジメントとガバナンス` に分類。

### 2.4. コンテナ

#### 2.4.1. AWS Copilot

- コンテナ化されたアプリケーションを AWS にデプロイ、管理するための CLI ツール。

#### 2.4.2. Amazon Elastic Container Registry (Amazon ECR)

##### 概要

- Docker コンテナイメージを安全に保存、管理、デプロイできるレジストリサービス。

#### 2.4.3. Amazon Elastic Container Service (Amazon ECS)

##### 概要

- コンテナのデプロイ、管理を簡単に行える AWS のスケーラブルなコンテナオーケストレーションサービス。

#### 2.4.4. Amazon Elastic Kubernetes Service (Amazon EKS)

##### 概要

- Kubernetes を使用したコンテナ管理を AWS 上でサポートするマネージドサービス。

### 2.5. データベース

#### 2.5.1. Amazon Aurora

##### 概要

- 高性能で高可用性を持つリレーショナルデータベースサービス。MySQL と PostgreSQL に互換性がある。
  - 標準的な MySQL データベースと比べて最大で 5 倍、標準的な PostgreSQL データベースと比べて最大で 3 倍高速化することが可能。

##### 主な機能

- Aurora Auto Scaling
  - シングルマスターレプリケーションを使用して、Aurora DB クラスターに対する急激な接続やワークロードの増加を処理。
- Aurora レプリカ
  - Aurora のリードレプリカ機能。15 台まで配置可能。

#### 2.5.2. Amazon Aurora Serverless

##### 概要

- 自動的にスケールする Aurora のサーバーレスオプション。

#### 2.5.3. Amazon DocumentDB (MongoDB 互換)

##### 概要

- MongoDB 互換の高可用性ドキュメントデータベースサービス。

#### 2.5.4. Amazon DynamoDB

##### 概要

- フルマネージドで高速、スケーラブルな NoSQL データベースサービス。
- 主キーでインデックスをつけられたデータを格納することができる。
- 1 バイトから最大 400KB までの範囲の項目への低レイテンシーの読み取りおよび書き込みアクセスが可能。
  - Web セッション情報やメタデータの保存に最適。

##### 主な機能

- DynamoDB Accelerator(DAX)
  - DAX を有効化することで、追加のキャッシュレイヤーによってミリセカンドからマイクロセカンドへの最大 10 倍のパフォーマンス向上を実現可能。
  - DAX はインメモリ型のキャッシュを利用しているため、特定のデータ領域処理を高速化出来るが、インメモリ型のキャッシュレイヤーは高コストであるため、常時利用しているとコストが高くなる。
- DynamoDB グローバルテーブル
  - マルチリージョンにマルチマスターデータベースをデプロイするための完全マネージド型のソリューション。
  - 複数リージョンに展開されたテーブルを同一のテーブルのように取り扱い、DynamoDB テーブルのデータ変更内容をすべてのテーブルに同時に反映する。
- DynamoDB ストリーム
  - DynamoDB テーブルに保存されたデータ項目の変更をキャプチャする機能
  - DynamoDB ストリームを有効化した後に、ユーザーが DynamoDB テーブルにデータを新規に追加すると、そのデータイベントをトリガーにして Lambda 関数を動作させるといったイベント起動型の処理を実行することが可能。
    - 例えば、データを別リージョンの DainamoDB へ自動的にレプリケーションすることが出来る。
  - DynamoDB テーブル内の項目レベルの変更の時系列シーケンスをキャプチャし、この情報を最大 24 時間ログに保存する。24 時間経過後はログが削除される。

#### 2.5.5. Amazon ElastiCache

##### 概要

- Redis または Memcached を使用したインメモリデータストアサービス。
- SQL クエリ処理結果をインメモリ DB に保持して高速化するために利用。
- Redis または Memcached のインメモリデータストアを利用できるマネージドサービス。

#### 2.5.6. Amazon MemoryDB for Redis

- Redis をベースにした高可用性、高耐障害性のインメモリデータベースサービス。

#### 2.5.7. Amazon RDS

##### 概要

- 複数のデータベースエンジン (MySQL、PostgreSQL、Oracle、MariaDB、SQL Server など) をサポートするリレーショナルデータベースサービス。

### 2.6. デベロッパーツール

#### 2.6.1. AWS Amplify

##### 概要

- ウェブおよびモバイルアプリケーションの構築、デプロイ、ホスティングを簡単に行えるフルマネージドサービス。
- SAA-C03 の試験ガイドでは `フロントエンドのウェブとモバイル` に分類。

#### 2.6.2. AWS Cloud9

##### 概要

- クラウドベースの統合開発環境 (IDE) を提供するサービス。

#### 2.6.3. AWS CloudShell

##### 概要

- ブラウザベースのシェル環境で AWS CLI を操作可能。

#### 2.6.4. AWS CodeArtifact

##### 概要

- ソフトウェアパッケージの管理と共有のためのリポジトリサービス。

#### 2.6.5. AWS CodeBuild

- ソースコードをコンパイルし、テストとビルドを実行するための完全マネージドサービス。

#### 2.6.6. AWS CodeCommit

##### 概要

- Git ベースのソースコードリポジトリをホストするマネージドサービス。

#### 2.6.7. AWS CodeDeploy

##### 概要

- ソフトウェアの自動デプロイメントをサポートするサービス。

#### 2.6.8. Amazon CodeGuru

##### 概要

- コードレビューとアプリケーションパフォーマンスチューニングのための ML ベースのサービス。

#### 2.6.9. AWS CodePipeline

##### 概要

- 継続的インテグレーションとデリバリー (CI/CD) のためのサービス。

#### 2.6.10. AWS CodeStar

##### 概要

- アプリケーション開発プロジェクトを管理するためのツールセット。

#### 2.6.11. Amazon CodeWhisperer

##### 概要

- AI を使用してコードスニペットを提案するツール。

#### 2.6.12. AWS X-Ray

##### 概要

- 分散トレース機能を提供し、アプリケーションのパフォーマンスとデバッグを支援するサービス。
- SAA-C03 の試験ガイドでは `フロントエンドのウェブとモバイル` に分類。

##### 主な機能

- トレースデータ
  - トレースデータを使用して、アプリケーションで使用されるサービスのマップを作成する。
  - トレースデータを使用すると、特定のサービスまたは問題について詳しく調査できる。
  - このデータは、アプリケーション内のサービス間の接続と、平均レイテンシーと障害率を含む各サービスの集計データのビューを提供する。

##### 公式ページ

- [AWS X-Ray の特徴](https://aws.amazon.com/jp/xray/features/)

### 2.7. マネジメントとガバナンス

#### 2.7.1. AWS AppConfig

##### 概要

- アプリケーション設定の管理とデプロイを行うサービス。

#### 2.7.2. AWS CLI

##### 概要

- AWS サービスをコマンドラインから操作するためのツール。

#### 2.7.3. AWS Cloud Development Kit (AWS CDK)

##### 概要

- プログラムコードで AWS リソースをプロビジョニングするためのフレームワーク。

#### 2.7.4. AWS CloudFormation

##### 概要

- インフラストラクチャをコードとして管理できるテンプレートベースのプロビジョニングサービス。

##### 主な機能

- テンプレート
  - AWSTemplateFormatVersion (形式バージョン) (任意)
    - テンプレートが準拠している AWS CloudFormation テンプレートバージョン。
    - テンプレート形式バージョンは API および WSDL バージョンとは関係なく変更可能。
  - Description (オプション)
    - テンプレートを説明するテキスト文字列。
    - このセクションは必ずテンプレートの Format Version セクションの後に記述する必要がある。
  - Metadata (オプション)
    - テンプレートに関する追加情報を提供するオブジェクト。
  - Parameters (任意)
    - 実行時に (スタックを作成または更新するとき)、テンプレートに渡すことができる値。
    - テンプレートの Resources および Outputs セクションのパラメータを参照可能。
  - Rules (オプション)
    - スタックの作成またはスタックの更新時に、テンプレートに渡されたパラメータまたはパラメータの組み合わせを検証する。
  - Mappings (任意)
    - 条件パラメータ値の指定に使用するキーと関連する値のマッピング (検索テーブルに類似したもの)。
    - Resources セクションと Outputs セクションで Fn::FindInMap 組み込み関数を使用することで、キーと対応する値を一致させることが可能。
  - Conditions (オプション)
    - 特定のリソースが作成されるかどうかや、スタックの作成または更新中に特定のリソースプロパティが値を割り当てられるかどうかの条件を規定する。
  - Transform (オプション)
    - サーバーレスアプリケーション (Lambda ベースアプリケーションとも呼ばれます) の場合は、使用する AWS Serverless Application Model (AWS SAM) のバージョンを指定する。
  - Resources (必須)
    - Amazon Elastic Compute Cloud インスタンスや Amazon Simple Storage Service バケットなど、スタックリソースとそのプロパティを指定する。
    - テンプレートの Resources および Outputs セクションのリソースを参照可能。
  - Outputs (任意)
    - スタックのプロパティを確認すると返される値について説明する。
    - たとえば、S3 バケット名の出力を宣言してから、aws cloudformation describe-stacks AWS CLI コマンドを呼び出して名前を表示することが可能。

##### 公式ページ

- [CloudFormation テンプレートセクション](https://docs.aws.amazon.com/ja_jp/AWSCloudFormation/latest/UserGuide/template-anatomy.html)

#### 2.7.5. AWS CloudTrail

##### 概要

- AWS アカウント内での API 呼び出しを記録し、監査を支援するサービス。

##### 主な機能

- イベント履歴
  - ガバナンス、コンプライアンス運用、およびリスク監査の目的で API コールを記録するために使用される。

##### 公式ページ

- [AWS CloudTrail とは](https://docs.aws.amazon.com/ja_jp/awscloudtrail/latest/userguide/cloudtrail-user-guide.html)
- [CloudTrail イベント履歴でのイベントの表示](https://docs.aws.amazon.com/ja_jp/awscloudtrail/latest/userguide/view-cloudtrail-events.html)

#### 2.7.6. Amazon CloudWatch

##### 概要

- AWS リソースやアプリケーションの監視とログ記録を提供するサービス。

#### 2.7.7. Amazon CloudWatch Logs

##### 概要

- ログデータの収集、モニタリング、分析を行うサービス。

#### 2.7.8. AWS Systems Manager

##### 概要

- AWS リソースとオンプレミス環境の運用管理を統合するサービス。

#### 2.7.9. AWS Trusted Advisor

##### 概要

- コスト、セキュリティ、パフォーマンス、耐障害性を最適化する推奨を提供するツール。
- AWS のベストプラクティスに従うように AWS のリソースをプロビジョニングするのに役立つガイダンスをリアルタイムで提供する。
- システム全体の使用状況をレポート可能。

##### 主な機能

##### 公式ページ

- [AWS Trusted Advisor](https://docs.aws.amazon.com/ja_jp/awssupport/latest/user/trusted-advisor.html)

### 2.8. ネットワークとコンテンツ配信

#### 2.8.1. Amazon API Gateway

##### 概要

- API の作成、配信、管理を簡単に行うためのサービス。
- サーバーなしに API ゲートウェイを利用できる。
- トラフィック管理、認可とアクセスコントロール、モニタリング、API バージョン管理などの API 管理を実施できる。
- 基本利用に対する料金は取られず、API コールと転送データ量に応じてのみ費用がかかる。
- SAA-C03 の試験ガイドでは `フロントエンドのウェブとモバイル` に分類。

##### 主な機能

- HTTP API
- Restful API
- WebSocket API

#### 2.8.2. Amazon CloudFront

##### 概要

- コンテンツをグローバルに迅速かつ安全に配信するコンテンツ配信ネットワーク（CDN）。
- ユーザーに近い位置にあるエッジロケーションにキャッシュを保持することで、高速のコンテンツ配信を実施する。

#### 2.8.3. Elastic Load Balancing (ELB)

##### 概要

- アプリケーションへのトラフィックを自動的に分散し、アプリケーションの高可用性を実現するロードバランシングサービス。

##### 主な機能

- ヘルスチェック
- クロスゾーン負荷分散
  - AZ 間の分散を均等に実施する
- 暗号化通信
- スティッキーセッション
  - ELB がサーバにリクエストを振り分ける際に Cookie を確認して特定のクライアントからのリクエストを特定のサーバに継続的に送信する
- Connection Draining
  - 既存の接続を開いたまま、登録解除または異常なインスタンスへの ELB のリクエスト送信を停止する
- ログ取得

#### 2.8.4. Amazon Route 53

##### 概要

- 高可用性でスケーラブルなドメインネームシステム (DNS) およびドメイン管理サービス。

##### 主な機能

- IP フローティング
  - 障害発生時にダウンタイムを無くすため、Elastic IP を自動で付け替える機能
- エイリアスレコード
  - Route 53 レコードに AWS リソースのエイリアスを登録することができる特別なレコード
  - レコードの種類
    - A レコード：IPv4 アドレス指定
    - AAAA レコード：IPv6 アドレス指定
    - MX レコード：メールサーバー指定
    - CNAME レコード：ドメイン名を別のドメイン名への関連付け
    - NS レコード：外部ベンダーで購入したドメインを Route53 に設定
- シャッフルシャーディング
  - IPv4 と IPv6 の両方のホストゾーンに 4 つのリゾルバー IP アドレスの一意のセットを提供する。
  - 何らかの理由でユーザークエリが失敗した場合、再試行時に正常に処理されるようになる。
- エニーキャスト ルーティング
  - ネットワークの近接度に基づいて DNS クエリを最も近いエッジロケーションに送信する。
  - エッジロケーションのグローバルに分散されたネットワークから動作させることで、ユーザーによるアプリケーションへのアクセスが可能なように支援する。

#### 2.8.5. Amazon VPC

##### 概要

- AWS クラウド内に分離された仮想ネットワーク環境を構築し、リソースをセキュアに管理するサービス。

##### 主な機能

- ゲートウェイ
  - インターネットゲートウェイ
  - NAT ゲートウェイ
    - 2 層アーキテクチャを構築する場合
      - WEB サーバーとなる EC2 インスタンスをパブリックサブネットに設置し、セキュリティグループにより HTTP プロトコルのターゲットに 0.0.0.0/0 を設定する。次に DB インスタンスのセキュリティグループにおいて 3306 ポートのターゲットに「WEB サーバーがホストされた EC2 インスタンスのセキュリティグループ」を指定する。
      - 【DB 毎の TCP IP 通信 ポート番号 】
        - MySQL： 3306
        - PostgreSQL： 5432
        - リモートデスクトップ：3389
  - Egress-Only Internet Gateway
  - カスタマーゲートウェイ
    - オンプレミス環境と接続する際に利用するゲートウェイ
    - オンプレミス側に設定
    - [カスタマーゲートウェイデバイス - AWS Site-to-Site VPN (amazon.com)](https://docs.aws.amazon.com/ja_jp/vpn/latest/s2svpn/your-cgw.html)
  - 仮想プライベートゲートウェイ
- CIDR ブロック
  - 許容ブロックサイズは、「/ 28」サブネットマスクから「/ 16」のサブネットマスクまで。
  - CIDR ブロックは、VPC に関連付けられている既存の CIDR ブロックと重複不可。

### 2.9. セキュリティ、アイデンティティ、コンプライアンス

#### 2.9.1. AWS Certificate Manager (ACM)

##### 概要

- SSL/TLS 証明書を簡単に取得、デプロイ、管理するサービス。

#### 2.9.2. Amazon Cognito

##### 概要

- ユーザー認証やデバイス認証を提供・簡素化するアイデンティティ(ID)管理サービス。

#### 2.9.3. AWS Identity and Access Management (IAM)

##### 概要

- AWS リソースへのアクセスを制御するためのユーザー、グループ、ポリシー管理サービス。

##### 主な機能

#### 2.9.4. AWS Key Management Service (AWS KMS)

##### 概要

- データを保護するための暗号化キーの作成と管理サービス。

#### 2.9.5. AWS Private Certificate Authority

##### 概要

- プライベート証明書を発行、管理するためのサービス。

#### 2.9.6. AWS Secrets Manager

##### 概要

- アプリケーションのシークレット (パスワードや API キーなどの機密情報) を安全に管理するためのサービス。

#### 2.9.7. AWS Security Token Service (AWS STS)

##### 概要

- AWS リソースへのアクセスをコントロールできる一時的なセキュリティ認証情報を持つ信頼されたユーザーを作成および提供するサービス。

##### 主な機能

- ウェブ ID フェデレーションによる認証
  - 外部 の ID プロバイダーを使用してアプリケーションにサインインすることがでる
  - OpenID Connect を利用する場合に利用
- SAML ID フェデレーションによる認証
  - SAML 2.0 (Security Assertion Markup Language 2.0)を利用する場合に利用

#### 2.9.8. AWS WAF

##### 概要

- アプリケーションを不正アクセスから保護するウェブアプリケーションファイアウォール。
- AWS フラストラクチャに対する DDoS 攻撃を緩和して、レイヤー 7 における DDoS 攻撃から WEB アプリケーションを保護する。
  - ユーザーが独自のウェブセキュリティルールを定義することによって、ウェブアプリケーションに対する特定のトラフィックを許可またはブロックすることができる。
- 悪意あるトラフィックをフィルタリング。

### 2.10. ストレージ

#### 2.10.1. Amazon Elastic Block Store (Amazon EBS)

##### 概要

- Amazon EC2 にアタッチ可能な、スケーラブルな高性能ブロックストレージ。
- EC2 インスタンスから Amazon EBS ボリュームをデタッチするには、明示的にデタッチ操作を実行する必要がある。

##### 主な機能

- スナップショット
  - EBS の利用状況に関係なく、非同期に作成することができる。
    - ベストプラクティスとしては、データに齟齬が発生しないためにも EBS ボリュームを停止した上でスナップショットを取得する方が良いとされている。

#### 2.10.2. Amazon Elastic File System (Amazon EFS)

##### 概要

- Linux インスタンス向けのスケーラブルな、フルマネージドのネットワークファイルシステム。

#### 2.10.3. Amazon S3

##### 概要

- データの保存と取得を可能にするスケーラブルで耐久性の高いオブジェクトストレージサービス。
- Amazon S3 に格納可能なデータの総量とオブジェクトの数には制限は無い。
- 個別の Amazon S3 オブジェクトのサイズは、最低 0 バイトから最大 5 TB まで。
- 1 つの PUT にアップロード可能なオブジェクトの最大サイズは 5 GB 。
  - 100 MB を超えるオブジェクトの場合は、マルチパートアップロード機能の利用を要検討。

##### 主な機能

- バケット
- バージョニング
- 静的 WEB ホスティング
  - Index.html を設定することで、静的 WEB サイトを構築可能。
  - 静的ウェブホスティング機能を有効化、パブリックアクセスブロックの無効化、バケットポリシーの設定が必要。
- マルチパートアップロード

#### 2.10.4. Amazon S3 Glacier

##### 概要

- データアーカイブと長期保存に最適な低コストストレージ。
- 保存データはデフォルトで暗号化される。
- 最大 5TB のラージオブジェクトの保存が可能。
  - 非構造化 BLOB データを保存するのに適している。

---

## 3. 参照文献とか

[^1]: [AWS Certified Developer - Associate (DVA-C02) 試験ガイド](https://d1.awsstatic.com/ja_JP/training-and-certification/docs-dev-associate/AWS-Certified-Developer-Associate_Exam-Guide.pdf)
[^2]: [【SAA-C03 版】AWS 認定ソリューションアーキテクト アソシエイト模擬試験問題集（6 回分 390 問）](https://www.udemy.com/course/aws-knan/?srsltid=AfmBOoroNztq6Qz5jycWJPyYldYoSzxEPPi25ErUVWqyok3liojzo_DQ&couponCode=NEWYEARCAREERJP)
[^3]: [時間がないけど AWS 認定試験に合格したい人に贈る効率の良い勉強法 #AWS](https://qiita.com/ozzy3/items/4fb249a77a579a6cbea3)
[^4]: [AWS 新資格 Machine Learning Engineer - Associate(MLA-C01)合格体験記](https://qiita.com/ec2_on_aws/items/cc4e245bf47a0d4d803b)
[^5]: [AWS 認定全冠を維持し続ける理由と 12 冠(13 冠、14 冠？)までの学習方法・資格の難易度まとめ －How to become an Japan AWS All Certifications Engineer(formerly known as APN ALL AWS Certifications Engineer)－](https://tech.nri-net.com/entry/all_aws_certifications_engineer)
[^6]: [AWS 認定 ソリューションアーキテクト – アソシエイト(AWS Certified Solutions Architect – Associate)の学習方法](https://tech.nri-net.com/entry/aws_certified_solutions_architect_associate)
