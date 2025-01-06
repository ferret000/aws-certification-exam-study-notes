# [勉強記録]AWS Certified Solutions Architect - Associate

## はじめに

- [SAA-C03] 合格に向けた勉強記録をまとめようと思います。
  - 合格したら、Qiitaに合格体験記として載せたい
- AWS資格受験において、どういった問題が出る？等の話は規則としてできないようになっているため、その点は載せていません。
  - [AWS 認定プログラムアグリーメント](https://d1.awsstatic.com/legal/AWS-Certification-Agreement/AWS_Certification_Program_Agreement_Translation_Japanese2.pdf)

## 筆者前提

- SE歴10数年のおじさんです。
- Java周りのアプリケーションエンジニアがメインでしたが、最近はAWSやDockerを利用した基盤構築をしたりしなかったりしています。
- この資格取得に向けて勉強するタイミングでは、下記のAWS認定を取得済です。
  - Foundational
    - [AWS Certified Cloud Practitioner[CLF-C01]](https://aws.amazon.com/jp/certification/certified-cloud-practitioner/?ch=sec&sec=rmg&d=1)
  - Associate
    - [AWS Certified Solutions Architect - Associate](https://aws.amazon.com/jp/certification/certified-solutions-architect-associate/?ch=sec&sec=rmg&d=1) ※失効済
- 今回は過去取得していたが失効した、SSAを再取得するために勉強を始めました。
  - しかも、アカウントを紛失したので過去実績も証明できず・・・

## [SAA-C03] の試験概要

- 試験概要([試験ガイド](https://d1.awsstatic.com/ja_JP/training-and-certification/docs-sa-assoc/AWS-Certified-Solutions-Architect-Associate_Exam-Guide.pdf)を gpt4o で要約)

### **試験概要**
AWS Certified Solutions Architect - Associate (SAA-C03) 試験は、ソリューションアーキテクトを対象とし、AWS Well-Architected フレームワークに基づくソリューション設計能力を評価します。以下のタスクに関する知識とスキルが求められます：
- 現在および将来のビジネス要件に対応する AWS サービスを活用したソリューションの設計。
- 安全性、耐障害性、高パフォーマンス、コスト最適化を実現したアーキテクチャの設計。
- 既存のソリューションのレビューおよび改善提案。

### **試験内容**
- **出題形式**：択一選択問題（正解1つ）および複数選択問題（正解2つ以上）。
- **問題数**：採点対象問題 50問、採点対象外問題 15問（全65問）。
- **合否基準**：スコア範囲は100～1000点、合格スコアは720点。

### **試験分野と比重**
1. **セキュアなアーキテクチャの設計（30%）**  
   - IAMやセキュリティベストプラクティスの活用。
   - セキュアなワークロードおよびデータ管理。
2. **弾力性に優れたアーキテクチャの設計（26%）**  
   - スケーラブルかつフォールトトレラントなシステム設計。
3. **高パフォーマンスなアーキテクチャの設計（24%）**  
   - ストレージ、コンピューティング、データベース、ネットワークの最適化。
4. **コストを最適化したアーキテクチャの設計（20%）**  
   - コスト効率の良いリソース利用と管理。

### **推奨される事前経験**
- AWS サービスを使用した1年以上の実務経験。

### **試験対象技術とサービス**
試験範囲に含まれる AWS サービスは、コンピューティング、ストレージ、ネットワーク、データベース、セキュリティ、コスト管理など多岐にわたります。詳細はガイドの付録に記載されています。
※[#Appendix] にまとめています。

## 試験比較(XXX vs YYY)

## 勉強方法

Udemyを中心に学習を進めます。

- AWS Skill Builder デジタルトレーニング
  - AWS Certified Solutions Architect – Associate Official Practice Question Set (SAA-C03 - Japanese)
      - 無料のサンプル問題
  - Exam Prep Standard Course: AWS Certified Solutions Architect - Associate (SAA-C03) (Japanese) 日本語実写版
    - 試験準備のための要点がまとめられているデジタルトレーニング
- Udemy
  - [【SAA-C03版】AWS 認定ソリューションアーキテクト アソシエイト模擬試験問題集（6回分390問）](https://www.udemy.com/course/aws-knan/?srsltid=AfmBOoroNztq6Qz5jycWJPyYldYoSzxEPPi25ErUVWqyok3liojzo_DQ&couponCode=NEWYEARCAREERJP)
    - 所属会社が Udemy business を契約しており、無料で受講できるものを選定しました。

## 所感

※試験受験後に更新予定

## Appendix

試験ガイドに記載されている試験対象技術とサービスについてまとめます

### **試験に出題される可能性のあるテクノロジーと概念**
- コンピューティング  
- コスト管理  
- データベース  
- 災害対策  
- 高パフォーマンス  
- マネジメントとガバナンス  
- マイクロサービスとコンポーネントの配信  
- 移行とデータ転送  
- ネットワーク、接続、コンテンツ配信  
- 回復性  
- セキュリティ  
- サーバーレスでイベント駆動型の設計原則  
- ストレージ  

### **範囲内の AWS のサービスと機能**

#### **分析**
- Amazon Athena  
- AWS Data Exchange  
- AWS Data Pipeline  
- Amazon EMR  
- AWS Glue  
- Amazon Kinesis  
- AWS Lake Formation  
- Amazon Managed Streaming for Apache Kafka (Amazon MSK)  
- Amazon OpenSearch Service  
- Amazon QuickSight  
- Amazon Redshift  

#### **アプリケーション統合**
- Amazon AppFlow  
- AWS AppSync  
- Amazon EventBridge  
- Amazon MQ  
- Amazon Simple Notification Service (Amazon SNS)  
- Amazon Simple Queue Service (Amazon SQS)  
- AWS Step Functions  

#### **AWS コスト管理**
- AWS Budgets  
- AWS Cost and Usage Report  
- AWS Cost Explorer  
- Savings Plans  

#### **コンピューティング**
- AWS Batch  
- Amazon EC2  
- Amazon EC2 Auto Scaling  
- AWS Elastic Beanstalk  
- AWS Outposts  
- AWS Serverless Application Repository  
- VMware Cloud on AWS  
- AWS Wavelength  

#### **コンテナ**
- Amazon ECS Anywhere  
- Amazon EKS Anywhere  
- Amazon EKS Distro  
- Amazon Elastic Container Registry (Amazon ECR)  
- Amazon Elastic Container Service (Amazon ECS)  
- Amazon Elastic Kubernetes Service (Amazon EKS)  

#### **データベース**
- Amazon Aurora  
- Amazon Aurora Serverless  
- Amazon DocumentDB (MongoDB 互換)  
- Amazon DynamoDB  
- Amazon ElastiCache  
- Amazon Keyspaces (Apache Cassandra 向け)  
- Amazon Neptune  
- Amazon Quantum Ledger Database (Amazon QLDB)  
- Amazon RDS  
- Amazon Redshift  

#### **デベロッパーツール**
- AWS X-Ray  

#### **フロントエンドのウェブとモバイル**
- AWS Amplify  
- Amazon API Gateway  
- AWS Device Farm  
- Amazon Pinpoint  

#### **機械学習**
- Amazon Comprehend  
- Amazon Forecast  
- Amazon Fraud Detector  
- Amazon Kendra  
- Amazon Lex  
- Amazon Polly  
- Amazon Rekognition  
- Amazon SageMaker  
- Amazon Textract  
- Amazon Transcribe  
- Amazon Translate  

#### **マネジメントとガバナンス**
- AWS Auto Scaling  
- AWS CloudFormation  
- AWS CloudTrail  
- Amazon CloudWatch  
- AWS CLI  
- AWS Compute Optimizer  
- AWS Config  
- AWS Control Tower  
- AWS Health Dashboard  
- AWS License Manager  
- Amazon Managed Grafana  
- Amazon Managed Service for Prometheus  
- AWS マネジメントコンソール  
- AWS Organizations  
- AWS Proton  
- AWS Service Catalog  
- AWS Systems Manager  
- AWS Trusted Advisor  
- AWS Well-Architected Tool  

#### **メディアサービス**
- Amazon Elastic Transcoder  
- Amazon Kinesis Video Streams  

#### **移行と転送**
- AWS Application Discovery Service  
- AWS Application Migration Service  
- AWS Database Migration Service (AWS DMS)  
- AWS DataSync  
- AWS Migration Hub  
- AWS Snow ファミリー  
- AWS Transfer Family  

#### **ネットワークとコンテンツ配信**
- AWS Client VPN  
- Amazon CloudFront  
- AWS Direct Connect  
- Elastic Load Balancing (ELB)  
- AWS Global Accelerator  
- AWS PrivateLink  
- Amazon Route 53  
- AWS Site-to-Site VPN  
- AWS Transit Gateway  
- Amazon VPC  

#### **セキュリティ、アイデンティティ、コンプライアンス**
- AWS Artifact  
- AWS Audit Manager  
- AWS Certificate Manager (ACM)  
- AWS CloudHSM  
- Amazon Cognito  
- Amazon Detective  
- AWS Directory Service  
- AWS Firewall Manager  
- Amazon GuardDuty  
- AWS IAM Identity Center (AWS Single Sign-On)  
- AWS Identity and Access Management (IAM)  
- Amazon Inspector  
- AWS Key Management Service (AWS KMS)  
- Amazon Macie  
- AWS Network Firewall  
- AWS Resource Access Manager (AWS RAM)  
- AWS Secrets Manager  
- AWS Security Hub  
- AWS Shield  
- AWS WAF  

#### **サーバーレス**
- AWS AppSync  
- AWS Fargate  
- AWS Lambda  

#### **ストレージ**
- AWS Backup  
- Amazon Elastic Block Store (Amazon EBS)  
- Amazon Elastic File System (Amazon EFS)  
- Amazon FSx (すべてのタイプに対応)  
- Amazon S3  
- Amazon S3 Glacier  
- AWS Storage Gateway  

---

## 参照文献とか

- [AWS Certified Solutions Architect - Associate (SAA-C03) 試験ガイド](https://d1.awsstatic.com/ja_JP/training-and-certification/docs-sa-assoc/AWS-Certified-Solutions-Architect-Associate_Exam-Guide.pdf)
- [時間がないけどAWS認定試験に合格したい人に贈る効率の良い勉強法 #AWS](https://qiita.com/ozzy3/items/4fb249a77a579a6cbea3)
- [AWS 新資格 Machine Learning Engineer - Associate(MLA-C01)合格体験記](https://qiita.com/ec2_on_aws/items/cc4e245bf47a0d4d803b)
- [AWS認定全冠を維持し続ける理由と12冠(13冠、14冠？)までの学習方法・資格の難易度まとめ －How to become an Japan AWS All Certifications Engineer(formerly known as APN ALL AWS Certifications Engineer)－](https://tech.nri-net.com/entry/all_aws_certifications_engineer)
- [AWS 認定 ソリューションアーキテクト – アソシエイト(AWS Certified Solutions Architect – Associate)の学習方法](https://tech.nri-net.com/entry/aws_certified_solutions_architect_associate)
- 
