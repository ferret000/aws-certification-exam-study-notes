# [DEA-C01]試験範囲内の AWS のサービスと機能<!-- omit in toc -->

## 1. はじめに

- [DEA-C01] AWS Certified Data Engineer - Associate の試験範囲内の AWS サービスと機能についてまとめます
- 試験概要は[**こちら**](./DEA-C01_勉強記録.md)を参照してください
- 記載内容は、ChatGPT、AWS 公式ページ[^1]、Udemy 講座の解説[^2]、その他 Web サイト[^3][^4][^5][^6]を基にしています。
  - ChatGPT に概要を追加させたものを記載。勉強を進める中で更新予定。

## 2. 範囲内の AWS のサービスと機能

### 2.1. 分析

#### 2.1.1. Amazon Athena

##### 概要

- 標準 SQL を使用して Simple Storage Service (Amazon S3) 内のデータを直接、シンプルに分析できるようにするインタラクティブなクエリサービス。
- サーバーレスのインタラクティブなクエリサービスで、S3 に保存されたデータに対して SQL を使用した分析が可能。

#### 2.1.2. Amazon EMR

##### 概要

- Apache Hadoop、Spark などを活用したビッグデータ処理プラットフォーム。

#### 2.1.3. AWS Glue

##### 概要

- フルマネージドの ETL（抽出、変換、ロード）サービスで、データカタログ機能も提供。

#### 2.1.4. AWS Glue DataBrew

##### 概要

- コード不要でデータのクレンジングと前処理を実行できるデータ準備ツール。

#### 2.1.5. AWS Lake Formation

##### 概要

- データレイクの構築と管理を容易にするサービスで、アクセス制御やカタログ管理も可能。

#### 2.1.6. Amazon Kinesis

##### 概要

- ストリーミングデータをリアルタイムで収集、処理するためのサービス。データ分析やストリーム処理に利用される。

#### 2.1.7. Amazon Kinesis Data Streams

##### 概要

- 大量のストリーミングデータをリアルタイムに収集して、ETL 処理などを実施した上で、他の AWS サービスに送信することができるリアルタイムデータ処理用のサービス。
- 1 秒以下のデータロードが達成できる性能があり、ストリーミングデータをリアルタイムに処理したり、表示させたい場合に利用
- サーバーレスで動作。
- データ処理アプリケーション（Kinesis Data Streams アプリケーション）を作成して使用。
  - アプリケーションは Kinesis Client Library (KCL) を活用して構築可能。
  - 実行環境には Amazon EC2 インスタンス を使用。

#### 2.1.8. Amazon Kinesis Data Firehose

##### 概要

- 工場のデバイスから送信されるストリームデータを取得して保存するソリューション。
- Amazon Kinesis Data Firehose のレコード形式の変換を有効にすることで、Amazon S3 バケットに送信するレコード方式に変換することが出来るが、これはデータ変換までは実施しない。Firehose ストリーム用に設定できる送信先は Amazon S3 のみ。
- データロードまで 60 秒必要となるため、ミリ秒単位の処理には利用できないが、データを変換してストレージ（例: Amazon S3）などに配信する用途には向いている。
  - Kinesis Data Streams からデータを受け取って処理を継続可能。
  - Lambda 関数 を組み込んでデータ変換処理を実行可能。

#### 2.1.9. Amazon Managed Service for Apache Flink

##### 概要

- Flink ベースのストリーミングデータ処理をフルマネージドで提供。

#### 2.1.10. Amazon Managed Streaming for Apache Kafka (Amazon MSK)

##### 概要

- Apache Kafka をマネージド環境で運用できるサービス。

#### 2.1.11. Amazon OpenSearch Service

##### 概要

- オープンソースの検索および分析エンジンである OpenSearch をマネージドで提供。ログ分析や検索エクスペリエンスに使用。
- Elasticsearch は今後サポートしない？

#### 2.1.12. Amazon QuickSight

##### 概要

- クラウドベースの BI（ビジネスインテリジェンス）ツールで、データの可視化が可能。

### 2.2. アプリケーション統合

#### 2.2.1. Amazon AppFlow

##### 概要

- GraphQL API を構築し、リアルタイムデータ同期と API 作成を容易にするサービス。
- SaaS アプリケーション間でデータを統合し、同期するサービス。

#### 2.2.2. Amazon EventBridge

##### 概要

- AWS サービスや独自アプリケーション間のイベントを接続・統合するための、サーバーレスなイベントバスサービス。
- アマゾン ウェブ サービスのリソースの変更を記述した、システムイベントのほぼリアルタイムのストリームを配信する。
- イベント駆動アーキテクチャのためのイベントバスサービス。

##### 主な機能

##### 公式ページ

- [Amazon EventBridge とは](https://docs.aws.amazon.com/ja_jp/eventbridge/latest/userguide/eb-what-is.html)
- [Amazon EventBridge イベント](https://docs.aws.amazon.com/ja_jp/eventbridge/latest/userguide/eb-events.html)

#### 2.2.3. Amazon Managed Workflows for Apache Airflow (Amazon MWAA)

##### 概要

- Apache Airflow のワークフローを AWS 上でマネージド提供。

#### 2.2.4. Amazon Simple Notification Service (Amazon SNS)

##### 概要

- メッセージ通知のためのパブリッシュ/サブスクライブモデルのメッセージングサービス。
- メッセージ配信やアプリケーション通知を提供するパブリッシュ/サブスクライブ型メッセージングサービス。

#### 2.2.5. Amazon Simple Queue Service (Amazon SQS)

##### 概要

- メッセージキューイングサービスで、非同期メッセージ処理が可能。
- 分散アプリケーション間での非同期メッセージ処理を簡単に実現するキューイングサービス。

#### 2.2.6. AWS Step Functions

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

### 2.3. クラウド財務管理

#### 2.3.1. AWS Budgets

##### 概要

- コスト管理と予算の監視ができるサービス。

#### 2.3.2. AWS Cost Explorer

##### 概要

- AWS リソースのコストと使用状況を分析するためのツール。

### 2.4. コンピューティング

#### 2.4.1. AWS Batch

##### 概要

- 大量のバッチ処理を自動スケーリングで管理するサービス。

#### 2.4.2. Amazon EC2

##### 概要

- 仮想マシンを提供するクラウドコンピューティングサービス。

#### 2.4.3. AWS Lambda

##### 概要

- サーバーレスコンピューティングでコードを実行できるサービス。

#### 2.4.4. AWS Serverless Application Model (AWS SAM)

##### 概要

- サーバーレスアプリケーションを開発・デプロイするためのフレームワーク。

### 2.5. コンテナ

#### 2.5.1. Amazon Elastic Container Registry (Amazon ECR)

##### 概要

- Docker コンテナのイメージ管理サービス。

#### 2.5.2. Amazon Elastic Container Service (Amazon ECS)

##### 概要

- コンテナオーケストレーションサービスで、Fargate との統合も可能。

#### 2.5.3. Amazon Elastic Kubernetes Service (Amazon EKS)

##### 概要

- Kubernetes クラスタを AWS 上でマネージド提供。

### 2.6. データベース

#### 2.6.1. Amazon DocumentDB (MongoDB 互換)

##### 概要

- MongoDB 互換のマネージドドキュメントデータベース。

#### 2.6.2. Amazon DynamoDB

##### 概要

- フルマネージドの NoSQL データベースで、高速でスケーラブル。

#### 2.6.3. Amazon Keyspaces (Apache Cassandra 向け)

##### 概要

- Apache Cassandra 互換のスケーラブルな NoSQL データベース。

#### 2.6.4. Amazon MemoryDB for Redis

##### 概要

- Redis 互換のインメモリデータベース。

#### 2.6.5. Amazon Neptune

##### 概要

- グラフデータベースで、RDF や Property Graph をサポート。

#### 2.6.6. Amazon RDS

##### 概要

- マネージドなリレーショナルデータベースサービス。

#### 2.6.7. Amazon Redshift

##### 概要

- クラウドデータウェアハウスで、大規模なデータ分析が可能。

### 2.7. デベロッパーツール

#### 2.7.1. AWS CLI

##### 概要

- AWS サービスを操作するためのコマンドラインインターフェース。

#### 2.7.2. AWS Cloud9

##### 概要

- クラウドベースの統合開発環境（IDE）。

#### 2.7.3. AWS Cloud Development Kit (AWS CDK)

##### 概要

- コードで AWS インフラを管理するための開発ツール。

#### 2.7.4. AWS CodeBuild

##### 概要

- ソースコードのビルドとテストを自動化。

#### 2.7.5. AWS CodeCommit

##### 概要

- Git ベースのコードリポジトリ管理サービス。

#### 2.7.6. AWS CodeDeploy

##### 概要

- アプリケーションのデプロイを自動化。

#### 2.7.7. AWS CodePipeline

##### 概要

- 継続的インテグレーション/デリバリー（CI/CD）を実現するサービス。

### 2.8. フロントエンドのウェブとモバイル

#### 2.8.1. Amazon API Gateway

##### 概要

- REST API や WebSocket API を提供するフルマネージドサービス。

### 2.9. 機械学習

#### 2.9.1. Amazon SageMaker

##### 概要

- 機械学習モデルの構築・トレーニング・デプロイを行うプラットフォーム。

### 2.10. マネジメントとガバナンス

#### 2.10.1. AWS CloudFormation

##### 概要

- インフラストラクチャをコードで管理するためのサービス。

#### 2.10.2. AWS CloudTrail

##### 概要

- AWS アカウントのアクティビティを記録する監査ツール。

#### 2.10.3. Amazon CloudWatch

##### 概要

- AWS リソースのモニタリングとログ管理。

#### 2.10.4. Amazon CloudWatch Logs

##### 概要

- CloudWatch のログストレージ機能。

#### 2.10.5. AWS Config

##### 概要

- リソースの構成変更を追跡・管理するサービス。

#### 2.10.6. Amazon Managed Grafana

##### 概要

- AWS 上で Grafana をマネージド提供。

#### 2.10.7. AWS Systems Manager

##### 概要

- インフラストラクチャ管理とオペレーション自動化のためのツール。

#### 2.10.8. AWS Well-Architected Tool

##### 概要

- AWS のベストプラクティスに基づいたアーキテクチャ評価ツール。

### 2.11. 移行と転送

#### 2.11.1. AWS Application Discovery Service

##### 概要

- オンプレミスのアプリケーションを分析し、AWS 移行を支援。

#### 2.11.2. AWS Application Migration Service

##### 概要

- オンプレミスのワークロードを AWS に移行するサービス。

#### 2.11.3. AWS Database Migration Service (AWS DMS)

##### 概要

- データベースを AWS へ移行。

#### 2.11.4. AWS DataSync

##### 概要

- オンプレミスと AWS 間でデータを転送。

#### 2.11.5. AWS Schema Conversion Tool (AWS SCT)

##### 概要

- 異なるデータベース間でスキーマ変換を行うツール。

#### 2.11.6. AWS Snow ファミリー

##### 概要

- 大量データを物理デバイスで AWS に転送。

#### 2.11.7. AWS Transfer Family

##### 概要

- SFTP/FTPS/FTP を使用して AWS へのデータ転送を管理。

### 2.12. ネットワークとコンテンツ配信

#### 2.12.1. Amazon CloudFront

##### 概要

- コンテンツ配信ネットワーク（CDN）。

#### 2.12.2. AWS PrivateLink

##### 概要

- AWS サービスへのプライベート接続。

#### 2.12.3. Amazon Route 53

##### 概要

- スケーラブルな DNS サービス。

#### 2.12.4. Amazon VPC

##### 概要

- 仮想ネットワーク環境を構築。

### 2.13. セキュリティ、アイデンティティ、コンプライアンス

#### 2.13.1. AWS Identity and Access Management (IAM)

##### 概要

- AWS リソースのアクセス管理。

#### 2.13.2. AWS Key Management Service (AWS KMS)

##### 概要

- データの暗号化キー管理。

#### 2.13.3. Amazon Macie

##### 概要

- 機密データの識別と保護。

#### 2.13.4. AWS Secrets Manager

##### 概要

- 認証情報の管理。

#### 2.13.5. AWS Shield

##### 概要

- DDoS 保護。

#### 2.13.6. AWS WAF

##### 概要

- Web アプリケーションファイアウォール。

### 2.14. ストレージ

#### 2.14.1. AWS Backup

##### 概要

- データのバックアップ管理。

#### 2.14.2. Amazon Elastic Block Store (Amazon EBS)

##### 概要

- EC2 用のストレージ。

#### 2.14.3. Amazon Elastic File System (Amazon EFS)

##### 概要

- マネージド NFS ストレージ。

#### 2.14.4. Amazon S3

##### 概要

- オブジェクトストレージサービス。

#### 2.14.5. Amazon S3 Glacier

##### 概要

- データアーカイブ用の低コストストレージ。

---

## 3. 参照文献とか

[^1]: [AWS Certified Data Engineer - Associate (DEA-C01) 試験ガイド](https://d1.awsstatic.com/ja_JP/training-and-certification/docs-data-engineer-associate/AWS-Certified-Data-Engineer-Associate_Exam-Guide.pdf)
[^2]: [Practice Exams | AWS Certified Data Engineer - Associate](https://www.udemy.com/course/practice-exams-aws-certified-data-engineer-associate-r/)
[^3]: [時間がないけど AWS 認定試験に合格したい人に贈る効率の良い勉強法 #AWS](https://qiita.com/ozzy3/items/4fb249a77a579a6cbea3)
[^4]: [AWS 新資格 Machine Learning Engineer - Associate(MLA-C01)合格体験記](https://qiita.com/ec2_on_aws/items/cc4e245bf47a0d4d803b)
[^5]: [AWS 認定全冠を維持し続ける理由と 12 冠(13 冠、14 冠？)までの学習方法・資格の難易度まとめ －How to become an Japan AWS All Certifications Engineer(formerly known as APN ALL AWS Certifications Engineer)－](https://tech.nri-net.com/entry/all_aws_certifications_engineer)
[^6]: [AWS 認定 ソリューションアーキテクト – アソシエイト(AWS Certified Solutions Architect – Associate)の学習方法](https://tech.nri-net.com/entry/aws_certified_solutions_architect_associate)
