# [勉強記録]AWS Certified Developer - Associate

## はじめに

- [DEA-C01] 合格に向けた勉強記録をまとめようと思います。
  - 合格したら、Qiita に合格体験記として載せたい
- AWS 資格受験において、どういった問題が出る？等の話は規則としてできないようになっているため、その点は載せていません。
  - [AWS 認定プログラムアグリーメント](https://d1.awsstatic.com/legal/AWS-Certification-Agreement/AWS_Certification_Program_Agreement_Translation_Japanese2.pdf)

## 筆者前提

- SE 歴 10 数年のおじさんです。
- Java 周りのアプリケーションエンジニアがメインでしたが、最近は AWS や Docker を利用した基盤構築をしたりしなかったりしています。
- AWS のサービスだと、下記あたりを業務で触ってました。
  - EC2、ECS、Lambda あたりのコンピューティング関連
  - S3、EBS、EFS などのストレージ関連
  - RDB、Aurora などの DB 関連
  - SQS、AmazonMQ などの非同期処理関連
  - Code ファミリーなどの CICD 関連
- 逆に、ネットワークやセキュリティ、機械学習、アカウント管理などは全然触っていません。
- この資格取得に向けて勉強するタイミングでは、下記の AWS 認定を取得済です。
  - Foundational
    - [AWS Certified Cloud Practitioner[CLF-C01]](https://aws.amazon.com/jp/certification/certified-cloud-practitioner/)
  - Associate
    - [AWS Certified Solutions Architect - Associate](https://aws.amazon.com/jp/certification/certified-solutions-architect-associate/)
    - [AWS Certified Developer - Associate](https://aws.amazon.com/jp/certification/certified-developer-associate/)

## [DEA-C01] の試験概要

- 試験概要(試験ガイド[^1]を ChatGPT 4o で要約)

### AWS Certified Data Engineer - Associate (DEA-C01) 試験概要

#### **試験の目的**

この試験は、AWS のデータエンジニアリングに関するスキルを評価し、以下の能力を検証します。

- データの取り込み、変換、パイプラインのオーケストレーション
- 適切なデータストアの選択、データモデルの設計、データライフサイクルの管理
- データパイプラインの運用・監視・最適化
- 認証・認可・データ暗号化・プライバシー・ガバナンスの実装

#### **受験対象者**

- データエンジニアリング分野で 2 ～ 3 年の実務経験
- データ取り込み、変換、モデリング、セキュリティ、スキーマ設計に関する知識
- 1 ～ 2 年以上の AWS サービスの実務経験

#### **試験形式**

- **問題形式**: 択一選択問題（1 つの正解）および複数選択問題（2 つ以上の正解）
- **問題数**: 採点対象の問題 50 問 + 採点対象外の問題 15 問
- **合格ライン**: 1000 点満点中 720 点

#### **試験内容と配分**

1. **データの取り込みと変換（34%）**

   - データの取り込み（ストリーミング・バッチ処理）
   - ETL パイプラインの構築と最適化
   - AWS サービスを用いたデータ変換
   - データパイプラインのオーケストレーション

2. **データストア管理（26%）**

   - 適切なデータストアの選択
   - データカタログとスキーマ管理
   - データライフサイクルの管理とアーカイブ

3. **データ運用とサポート（22%）**

   - データ処理の自動化
   - AWS を活用したデータ分析とモニタリング
   - データパイプラインの保守とデータ品質の確保

4. **データセキュリティとガバナンス（18%）**
   - 認証・認可の実装
   - データの暗号化とマスキング
   - 監査ログの管理とデータプライバシー対策

#### **推奨知識**

- **IT スキル**: ETL パイプライン構築、Git の使用、データレイク管理、ネットワーク・ストレージの基本
- **AWS スキル**: AWS データ関連サービスの理解、データ暗号化・ガバナンス、SQL クエリの実行

#### **試験対象の AWS サービス**

- **データ処理**: AWS Glue、Amazon EMR、Amazon Kinesis、AWS DMS
- **ストレージ**: Amazon S3、Amazon Redshift、DynamoDB
- **セキュリティ**: AWS IAM、AWS KMS、Amazon Macie
- **分析**: Amazon Athena、Amazon QuickSight、AWS Glue DataBrew

#### **試験対象外の内容**

- AI/ML の実装
- 特定のプログラミング言語の知識
- ビジネス上の意思決定に関する分析

この試験は、AWS データエンジニアとしてのスキルを証明するための認定資格であり、データパイプラインの構築や管理を中心とした内容になっています。

---

## 勉強方法

Udemy を中心に学習を進めます。

- AWS Skill Builder デジタルトレーニング
  - Exam Prep Standard Course: AWS Certified Developer - Associate (DEA-C01) (日本語)
    - 試験準備のための要点がまとめられているデジタルトレーニング
  - AWS Certified Developer - Associate Official Practice Question Set (DEA-C01 - 日本語)
    - 無料のサンプル問題
- Udemy
  - [Practice Exams | AWS Certified Data Engineer - Associate](https://www.udemy.com/course/practice-exams-aws-certified-data-engineer-associate-r/)
    - 所属会社が Udemy business を契約しており、無料で受講できるものを選定しました。
    - 日本語対応で良さそうなものが無かったため、今回は英語のものを選定しています。

## 所感

※受験後に更新予定

## Appendix

試験ガイドに記載されている試験対象技術とサービスについてまとめます

### **試験に出題される可能性のあるテクノロジーと概念**

#### **データ処理とパイプライン**

- ETL（Extract, Transform, Load）
- ストリーミングデータ処理
- バッチデータ処理
- データ取り込みパターン（頻度、履歴管理）
- データパイプラインのオーケストレーション（Apache Airflow, AWS Step Functions）
- ステートフル vs ステートレスデータ処理
- フォーマット変換（CSV, Parquet, JSON）
- スロットリングとレート制限（DynamoDB, Amazon RDS, Kinesis）
- SQL クエリの最適化

#### **データストアと管理**

- ストレージプラットフォームと特性（Amazon S3, Amazon Redshift, DynamoDB）
- データカタログとメタデータ管理（AWS Glue Data Catalog, Apache Hive Metastore）
- データモデリング（スキーマ設計、正規化、非正規化）
- データライフサイクル管理（ホットデータ、コールドデータ）
- インデックス作成、パーティショニング、圧縮

#### **データ運用とサポート**

- API コールによるデータ処理の自動化
- クエリとデータ分析（Athena, QuickSight, Redshift）
- モニタリングとログ管理（CloudWatch, CloudTrail）
- データ品質確保（プロファイリング、スキュー管理、データ検証）

#### **セキュリティとガバナンス**

- 認証と認可（IAM, AWS Secrets Manager, Lake Formation）
- データ暗号化（AWS KMS, S3 SSE, クライアントサイド暗号化）
- 監査ログの管理（CloudTrail, OpenSearch）
- データプライバシーとコンプライアンス（PII データの保護、データ主権）

---

### **範囲内の AWS のサービスと機能**

#### **分析**

- Amazon Athena
- Amazon EMR
- AWS Glue
- AWS Glue DataBrew
- AWS Lake Formation
- Amazon Kinesis Data Firehose
- Amazon Kinesis Data Streams
- Amazon Managed Service for Apache Flink
- Amazon Managed Streaming for Apache Kafka (Amazon MSK)
- Amazon OpenSearch Service
- Amazon QuickSight

#### **アプリケーション統合**

- Amazon AppFlow
- Amazon EventBridge
- Amazon Managed Workflows for Apache Airflow (Amazon MWAA)
- Amazon Simple Notification Service (Amazon SNS)
- Amazon Simple Queue Service (Amazon SQS)
- AWS Step Functions

#### **クラウド財務管理**

- AWS Budgets
- AWS Cost Explorer

#### **コンピューティング**

- AWS Batch
- Amazon EC2
- AWS Lambda
- AWS Serverless Application Model (AWS SAM)

#### **コンテナ**

- Amazon Elastic Container Registry (Amazon ECR)
- Amazon Elastic Container Service (Amazon ECS)
- Amazon Elastic Kubernetes Service (Amazon EKS)

#### **データベース**

- Amazon DocumentDB (MongoDB 互換)
- Amazon DynamoDB
- Amazon Keyspaces (Apache Cassandra 向け)
- Amazon MemoryDB for Redis
- Amazon Neptune
- Amazon RDS
- Amazon Redshift

#### **デベロッパーツール**

- AWS CLI
- AWS Cloud9
- AWS Cloud Development Kit (AWS CDK)
- AWS CodeBuild
- AWS CodeCommit
- AWS CodeDeploy
- AWS CodePipeline

#### **フロントエンドのウェブとモバイル**

- Amazon API Gateway

#### **機械学習**

- Amazon SageMaker

#### **マネジメントとガバナンス**

- AWS CloudFormation
- AWS CloudTrail
- Amazon CloudWatch
- Amazon CloudWatch Logs
- AWS Config
- Amazon Managed Grafana
- AWS Systems Manager
- AWS Well-Architected Tool

#### **移行と転送**

- AWS Application Discovery Service
- AWS Application Migration Service
- AWS Database Migration Service (AWS DMS)
- AWS DataSync
- AWS Schema Conversion Tool (AWS SCT)
- AWS Snow ファミリー
- AWS Transfer Family

#### **ネットワークとコンテンツ配信**

- Amazon CloudFront
- AWS PrivateLink
- Amazon Route 53
- Amazon VPC

#### **セキュリティ、アイデンティティ、コンプライアンス**

- AWS Identity and Access Management (IAM)
- AWS Key Management Service (AWS KMS)
- Amazon Macie
- AWS Secrets Manager
- AWS Shield
- AWS WAF

#### **ストレージ**

- AWS Backup
- Amazon Elastic Block Store (Amazon EBS)
- Amazon Elastic File System (Amazon EFS)
- Amazon S3
- Amazon S3 Glacier

---

## 参照文献とか

[^1]: [AWS Certified Data Engineer - Associate (DEA-C01) 試験ガイド](https://d1.awsstatic.com/ja_JP/training-and-certification/docs-data-engineer-associate/AWS-Certified-Data-Engineer-Associate_Exam-Guide.pdf)

- [時間がないけど AWS 認定試験に合格したい人に贈る効率の良い勉強法 #AWS](https://qiita.com/ozzy3/items/4fb249a77a579a6cbea3)
- [AWS 新資格 Machine Learning Engineer - Associate(MLA-C01)合格体験記](https://qiita.com/ec2_on_aws/items/cc4e245bf47a0d4d803b)
- [AWS 認定全冠を維持し続ける理由と 12 冠(13 冠、14 冠？)までの学習方法・資格の難易度まとめ －How to become an Japan AWS All Certifications Engineer(formerly known as APN ALL AWS Certifications Engineer)－](https://tech.nri-net.com/entry/all_aws_certifications_engineer)
- [AWS 認定 ソリューションアーキテクト – アソシエイト(AWS Certified Solutions Architect – Associate)の学習方法](https://tech.nri-net.com/entry/aws_certified_solutions_architect_associate)
-
