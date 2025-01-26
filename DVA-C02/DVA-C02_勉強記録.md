# [勉強記録]AWS Certified Developer - Associate

## はじめに

- [DVA-C02] 合格に向けた勉強記録をまとめようと思います。
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
    - [AWS Certified Cloud Practitioner[CLF-C01]](https://aws.amazon.com/jp/certification/certified-cloud-practitioner/?ch=sec&sec=rmg&d=1)
  - Associate
    - [AWS Certified Solutions Architect - Associate](https://aws.amazon.com/jp/certification/certified-solutions-architect-associate/?ch=sec&sec=rmg&d=1)

## [DVA-C02] の試験概要

- 試験概要(試験ガイド[^1]を ChatGPT 4o で要約)

### 試験概要

AWS Certified Developer - Associate (DVA-C02) 試験は、AWS クラウドベースのアプリケーション開発、テスト、デプロイ、デバッグに関するスキルを検証するものです。試験は以下の分野で構成されています。

1. **AWS サービスによる開発 (32%)**

   - アプリケーションコードの開発、最適化
   - Lambda やデータストアの利用

2. **セキュリティ (26%)**

   - 認証・認可
   - データの暗号化
   - 機密データの管理

3. **デプロイ (24%)**

   - アプリケーションの準備・テスト
   - CI/CD ワークフローの利用

4. **トラブルシューティングと最適化 (18%)**
   - ログとモニタリングによる問題解決
   - パフォーマンス最適化

### 試験形式

- **解答タイプ**: 単一選択問題、複数選択問題
- **設問数**: 採点対象 50 問 + 採点対象外 15 問
- **合格スコア**: 100 ～ 1,000 スコア中 720

### 推奨知識

- **IT スキル**: プログラミング言語、高度なアプリケーションライフサイクル管理の知識
- **AWS 知識**: AWS API、CLI、SDK、CI/CD パイプラインの操作経験

### 対象外の範囲

- システムアーキテクチャ設計
- IAM ユーザー管理
- ネットワークインフラ構築 (例: Amazon VPC)

## 勉強方法

Udemy を中心に学習を進めます。

- AWS Skill Builder デジタルトレーニング
  - Exam Prep Standard Course: AWS Certified Developer - Associate (DVA-C02) (日本語)
    - 試験準備のための要点がまとめられているデジタルトレーニング
  - AWS Certified Developer - Associate Official Practice Question Set (DVA-C02 - 日本語)
    - 無料のサンプル問題
- Udemy
  - [【０１版】AWS 認定デベロッパー アソシエイト模擬試験問題集（5 回分 325 問）]
    - 所属会社が Udemy business を契約しており、無料で受講できるものを選定しました。
    - Udemy business で選択できるものの中で DVA-C02 に対応した演習テストが無かったのでこちらを採用しています。

## 所感

※受験後に更新予定

## Appendix

試験ガイドに記載されている試験対象技術とサービスについてまとめます

### 試験に出題される可能性のあるテクノロジーと概念

- 分析
- アプリケーション統合
- コンピューティング
- コンテナ
- コストと容量管理
- データベース
- デベロッパーツール
- マネジメントとガバナンス
- ネットワークとコンテンツ配信
- セキュリティ、アイデンティティ、コンプライアンス
- ストレージ

---

### 範囲内の AWS のサービスと機能

各サービスと機能の詳細（勉強記録）は[**こちら**](./DVA-C02_試験範囲内のAWSのサービスと機能.md)を参照してください。

#### 分析

- Amazon Athena
- Amazon Kinesis
- Amazon OpenSearch Service

#### アプリケーション統合

- AWS AppSync
- Amazon EventBridge
- Amazon Simple Notification Service (Amazon SNS)
- Amazon Simple Queue Service (Amazon SQS)
- AWS Step Functions

#### コンピューティング

- Amazon EC2
- AWS Elastic Beanstalk
- AWS Lambda
- AWS Serverless Application Model (AWS SAM)

#### コンテナ

- AWS Copilot
- Amazon Elastic Container Registry (Amazon ECR)
- Amazon Elastic Container Service (Amazon ECS)
- Amazon Elastic Kubernetes Service (Amazon EKS)

#### データベース

- Amazon Aurora
- Amazon DynamoDB
- Amazon ElastiCache
- Amazon MemoryDB for Redis
- Amazon RDS

#### デベロッパーツール

- AWS Amplify
- AWS Cloud9
- AWS CloudShell
- AWS CodeArtifact
- AWS CodeBuild
- AWS CodeCommit
- AWS CodeDeploy
- Amazon CodeGuru
- AWS CodePipeline
- AWS CodeStar
- Amazon CodeWhisperer
- AWS X-Ray

#### マネジメントとガバナンス

- AWS AppConfig
- AWS CLI
- AWS Cloud Development Kit (AWS CDK)
- AWS CloudFormation
- AWS CloudTrail
- Amazon CloudWatch
- Amazon CloudWatch Logs
- AWS Systems Manager

#### ネットワークとコンテンツ配信

- Amazon API Gateway
- Amazon CloudFront
- Elastic Load Balancing (ELB)
- Amazon Route 53
- Amazon VPC

#### セキュリティ、アイデンティティ、コンプライアンス

- AWS Certificate Manager (ACM)
- Amazon Cognito
- AWS Identity and Access Management (IAM)
- AWS Key Management Service (AWS KMS)
- AWS Private Certificate Authority
- AWS Secrets Manager
- AWS Security Token Service (AWS STS)
- AWS WAF

#### ストレージ

- Amazon Elastic Block Store (Amazon EBS)
- Amazon Elastic File System (Amazon EFS)
- Amazon S3
- Amazon S3 Glacier

---

## 参照文献とか

[^1]: [AWS Certified Developer - Associate (DVA-C02) 試験ガイド](https://d1.awsstatic.com/ja_JP/training-and-certification/docs-dev-associate/AWS-Certified-Developer-Associate_Exam-Guide.pdf)

- [時間がないけど AWS 認定試験に合格したい人に贈る効率の良い勉強法 #AWS](https://qiita.com/ozzy3/items/4fb249a77a579a6cbea3)
- [AWS 新資格 Machine Learning Engineer - Associate(MLA-C01)合格体験記](https://qiita.com/ec2_on_aws/items/cc4e245bf47a0d4d803b)
- [AWS 認定全冠を維持し続ける理由と 12 冠(13 冠、14 冠？)までの学習方法・資格の難易度まとめ －How to become an Japan AWS All Certifications Engineer(formerly known as APN ALL AWS Certifications Engineer)－](https://tech.nri-net.com/entry/all_aws_certifications_engineer)
- [AWS 認定 ソリューションアーキテクト – アソシエイト(AWS Certified Solutions Architect – Associate)の学習方法](https://tech.nri-net.com/entry/aws_certified_solutions_architect_associate)
-
