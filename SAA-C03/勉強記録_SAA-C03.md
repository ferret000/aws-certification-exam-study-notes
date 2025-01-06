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

ChatGPTに概要を追加させたものを記載。ファクトチェックは未実施なので、勉強を進める中で更新予定。

#### **分析**
- Amazon Athena  
  - SQLを使用してS3に保存されたデータを簡単にクエリ可能にするサーバーレスのインタラクティブなクエリサービス。
- AWS Data Exchange  
  - サードパーティのデータを簡単に見つけ、サブスクライブして利用できるデータ共有サービス。
- AWS Data Pipeline  
  - データの移動や変換を自動化する、スケーラブルなデータ処理サービス。
- Amazon EMR  
  - ビッグデータ処理用のフレームワーク（Hadoop、Sparkなど）を簡単にセットアップ、管理できるサービス。
- AWS Glue  
  - データの準備、変換、カタログ化を簡単に行うためのサーバーレスETL（抽出・変換・ロード）サービス。
- Amazon Kinesis  
  - ストリーミングデータをリアルタイムで収集、処理するサービス。
- AWS Lake Formation  
  - データレイクの構築とセキュリティ設定を迅速に行うためのサービス。
- Amazon Managed Streaming for Apache Kafka (Amazon MSK)  
  - Apache Kafkaのセットアップと運用を簡素化するマネージド型サービス。
- Amazon OpenSearch Service  
  - OpenSearchとElasticsearchを使用したデータの検索、可視化、分析を可能にするサービス。
- Amazon QuickSight  
  - データの可視化とダッシュボード作成をサポートするBI（ビジネスインテリジェンス）サービス。
- Amazon Redshift  
  - ペタバイトスケールのデータウェアハウスソリューションで、高速クエリが可能。

#### **アプリケーション統合**
- Amazon AppFlow  
  - SaaSアプリケーションとAWSサービス間の安全なデータ転送を簡単に設定できるサービス。
- AWS AppSync  
  - GraphQL APIを構築し、リアルタイムデータ更新を提供するためのサービス。
- Amazon EventBridge  
  - サーバーレスのイベントバスサービスで、アプリケーションやSaaS間のイベント駆動型の統合を可能にする。
- Amazon MQ  
  - オープンソースのメッセージブローカー（ActiveMQ、RabbitMQ）をサポートするマネージド型サービス。
- Amazon Simple Notification Service (Amazon SNS)  
  - メッセージ配信やアプリケーション通知を提供するパブリッシュ/サブスクライブ型サービス。
- Amazon Simple Queue Service (Amazon SQS)  
  - 分散アプリケーション間での非同期メッセージ処理を簡単に実現するキューイングサービス。
- AWS Step Functions  
  - サーバーレスのワークフローオーケストレーションサービスで、複雑なプロセスを簡単に自動化。

#### **AWS コスト管理**
- AWS Budgets  
  - AWSのコストと使用量を追跡し、予算に基づいてアラートを設定できるツール。
- AWS Cost and Usage Report  
  - AWSリソースの利用状況とコストの詳細レポートを提供するサービス。
- AWS Cost Explorer  
  - コストのトレンドを視覚化し、将来のコストを予測するためのツール。
- Savings Plans  
  - コンピューティングコストを最大72%削減可能な柔軟な料金プラン。

#### **コンピューティング**
- AWS Batch  
  - 大量のバッチコンピューティングジョブを効率的に実行できるフルマネージドサービス。
- Amazon EC2  
  - 仮想サーバーをプロビジョニングして、アプリケーションをホストできるクラウドインフラサービス。
- Amazon EC2 Auto Scaling  
  - トラフィックや負荷に応じてEC2インスタンスを自動的に増減するサービス。
- AWS Elastic Beanstalk  
  - アプリケーションのデプロイとスケーリングを簡素化するプラットフォームサービス。
- AWS Outposts  
  - AWSインフラとサービスをオンプレミス環境で利用可能にするソリューション。
- AWS Serverless Application Repository  
  - サーバーレスアプリケーションの共有とデプロイを簡単に行えるリポジトリサービス。
- VMware Cloud on AWS  
  - VMware環境をAWS上に展開して、オンプレミスの拡張を簡単にするサービス。
- AWS Wavelength  
  - 5Gネットワークエッジにクラウドサービスを提供するためのインフラストラクチャ。

#### **コンテナ**
- Amazon ECS Anywhere  
  - AWSのElastic Container Serviceをオンプレミス環境でも利用可能にする拡張サービス。
- Amazon EKS Anywhere  
  - Kubernetesをオンプレミス環境で利用できるようにするAWSの拡張サービス。
- Amazon EKS Distro  
  - KubernetesのAWSが管理するディストリビューションを利用できるサービス。
- Amazon Elastic Container Registry (Amazon ECR)  
  - Dockerコンテナイメージを保存、管理、デプロイするためのマネージド型サービス。
- Amazon Elastic Container Service (Amazon ECS)  
  - コンテナのデプロイ、管理を簡単に行えるAWSのスケーラブルなサービス。
- Amazon Elastic Kubernetes Service (Amazon EKS)  
  - KubernetesクラスタをAWS上でフルマネージドで運用できるサービス。

#### **データベース**
- Amazon Aurora  
  - 高性能で高可用性を持つリレーショナルデータベースサービス。
- Amazon Aurora Serverless  
  - 自動的にスケールするAuroraのサーバーレスオプション。
- Amazon DocumentDB (MongoDB 互換)  
  - MongoDB互換の高可用性ドキュメントデータベースサービス。
- Amazon DynamoDB  
  - 高速でスケーラブルなNoSQLデータベースサービス。
- Amazon ElastiCache  
  - RedisまたはMemcachedを使用したインメモリデータストアサービス。
- Amazon Keyspaces (Apache Cassandra 向け)  
  - Apache Cassandra互換のスケーラブルなキーバリューストア。
- Amazon Neptune  
  - グラフデータを扱うためのマネージド型グラフデータベースサービス。
- Amazon Quantum Ledger Database (Amazon QLDB)  
  - 変更履歴を追跡可能なジャーナリングデータベース。
- Amazon RDS  
  - MySQL、PostgreSQL、Oracleなど複数のリレーショナルデータベースエンジンをサポートするマネージドサービス。
- Amazon Redshift  
  - 高速でスケーラブルなデータウェアハウスサービス。

#### **デベロッパーツール**
- AWS X-Ray  
  - 分散トレース機能を提供し、アプリケーションのパフォーマンスとデバッグを支援するサービス。

#### **フロントエンドのウェブとモバイル**
- AWS Amplify  
  - ウェブおよびモバイルアプリケーションの構築、デプロイ、ホスティングを簡単に行えるフルマネージドサービス。
- Amazon API Gateway  
  - APIの作成、配信、管理を簡単に行うためのサービス。
- AWS Device Farm  
  - 実際のデバイスでアプリをテストするためのモバイルアプリケーションテストサービス。
- Amazon Pinpoint  
  - マーケティングやユーザーエンゲージメントのためのカスタマイズメッセージングサービス。

#### **機械学習**
- Amazon Comprehend  
  - 自然言語処理を使用してテキストデータから洞察を抽出するサービス。
- Amazon Forecast  
  - 機械学習を利用して時系列データの予測を行うサービス。
- Amazon Fraud Detector  
  - 不正検出モデルを作成し、アプリケーションに統合するサービス。
- Amazon Kendra  
  - 機械学習を利用したインテリジェントな検索サービス。
- Amazon Lex  
  - 会話型インターフェース（チャットボット）を構築するサービス。
- Amazon Polly  
  - テキストを自然な音声に変換するサービス。
- Amazon Rekognition  
  - 画像や動画から顔、オブジェクト、シーンを検出するサービス。
- Amazon SageMaker  
  - 機械学習モデルの構築、トレーニング、デプロイを簡単にするサービス。
- Amazon Textract  
  - ドキュメント内のテキストやデータを自動的に抽出するサービス。
- Amazon Transcribe  
  - 音声をテキストに変換するサービス。
- Amazon Translate  
  - テキストを異なる言語に翻訳するサービス。

#### **マネジメントとガバナンス**
- AWS Auto Scaling  
  - リソースの負荷に応じてスケーリングを自動化するサービス。
- AWS CloudFormation  
  - インフラストラクチャをコードで管理するためのツール。
- AWS CloudTrail  
  - AWSアカウント内でのAPI呼び出しを記録し、監査を支援するサービス。
- Amazon CloudWatch  
  - AWSリソースやアプリケーションの監視とログ記録を提供するサービス。
- AWS CLI  
  - AWSサービスをコマンドラインから操作するためのツール。
- AWS Compute Optimizer  
  - コンピューティングリソースのコストと性能を最適化する推奨を提供するサービス。
- AWS Config  
  - リソースの構成変更を追跡し、コンプライアンスの監視をサポートするサービス。
- AWS Control Tower  
  - マルチアカウントのAWS環境を管理するためのガバナンスサービス。
- AWS Health Dashboard  
  - AWSサービスの状態をリアルタイムで確認するためのダッシュボード。
- AWS License Manager  
  - ソフトウェアライセンスの管理と監視を支援するサービス。
- Amazon Managed Grafana  
  - データの可視化とダッシュボード作成を行うGrafanaのマネージド型サービス。
- Amazon Managed Service for Prometheus  
  - メトリクスのモニタリングとアラートに特化したPrometheusのマネージドサービス。
- AWS マネジメントコンソール  
  - AWSリソースをブラウザから操作するためのGUI。
- AWS Organizations  
  - 複数のAWSアカウントを一元管理するサービス。
- AWS Proton  
  - マイクロサービスのインフラをテンプレートとして管理するサービス。
- AWS Service Catalog  
  - ITサービスを組織内で提供するためのツール。
- AWS Systems Manager  
  - AWSリソースとオンプレミス環境の運用管理を統合するサービス。
- AWS Trusted Advisor  
  - コスト、セキュリティ、パフォーマンス、耐障害性を最適化する推奨を提供するツール。
- AWS Well-Architected Tool  
  - AWSベストプラクティスに基づいてアーキテクチャを評価するためのツール。

#### **メディアサービス**
- Amazon Elastic Transcoder  
  - 動画や音声ファイルを異なるフォーマットに変換するメディアトランスコーディングサービス。
- Amazon Kinesis Video Streams  
  - ビデオデータをストリームで収集、処理、保存するためのサービス。

#### **移行と転送**
- AWS Application Discovery Service  
  - オンプレミス環境を評価し、AWS移行の計画をサポートするサービス。
- AWS Application Migration Service  
  - アプリケーションをAWSへ簡単かつ迅速に移行するためのリフト＆シフトサービス。
- AWS Database Migration Service (AWS DMS)  
  - データベースを最小限のダウンタイムでAWSに移行するためのサービス。
- AWS DataSync  
  - オンプレミスとAWS間でデータを迅速に転送するサービス。
- AWS Migration Hub  
  - 移行プロジェクトを統合的に管理し、進捗を可視化するツール。
- AWS Snow ファミリー  
  - 大規模データを物理的にAWSに移行するためのハードウェアデバイス群（Snowcone、Snowball、Snowmobile）。
- AWS Transfer Family  
  - SFTP、FTPS、FTPプロトコルをサポートするマネージド型ファイル転送サービス。

#### **ネットワークとコンテンツ配信**
- AWS Client VPN  
  - AWSクラウドとオンプレミス環境を安全に接続するためのVPNサービス。
- Amazon CloudFront  
  - コンテンツをグローバルに迅速かつ安全に配信するコンテンツ配信ネットワーク（CDN）。
- AWS Direct Connect  
  - オンプレミス環境とAWS間を専用回線で接続するサービス。
- Elastic Load Balancing (ELB)  
  - トラフィックを分散してアプリケーションの高可用性を実現するロードバランシングサービス。
- AWS Global Accelerator  
  - グローバルユーザーに対してアプリケーションのパフォーマンスと可用性を向上させるサービス。
- AWS PrivateLink  
  - VPC間やAWSサービス間で安全なプライベート接続を提供するサービス。
- Amazon Route 53  
  - 高可用性でスケーラブルなDNSおよびドメイン管理サービス。
- AWS Site-to-Site VPN  
  - オンプレミスネットワークとAWSを接続するIPsec VPNサービス。
- AWS Transit Gateway  
  - 複数のVPCやオンプレミス環境を統合的に接続するサービス。
- Amazon VPC  
  - AWS内に仮想ネットワークを作成し、リソースをセキュアに管理するサービス。

#### **セキュリティ、アイデンティティ、コンプライアンス**
- AWS Artifact  
  - AWSのコンプライアンスレポートやセキュリティ文書を提供するサービス。
- AWS Audit Manager  
  - AWSリソースの使用状況を監査し、コンプライアンス報告を簡素化するツール。
- AWS Certificate Manager (ACM)  
  - SSL/TLS証明書を簡単に取得、デプロイ、管理するサービス。
- AWS CloudHSM  
  - データの暗号化キーを管理するハードウェアセキュリティモジュール（HSM）。
- Amazon Cognito  
  - ユーザー認証とアプリケーションのセキュリティを簡素化するID管理サービス。
- Amazon Detective  
  - セキュリティ問題の根本原因を調査するためのサービス。
- AWS Directory Service  
  - Microsoft Active Directoryと互換性のあるディレクトリサービス。
- AWS Firewall Manager  
  - AWS WAF、Shield Advancedなどのセキュリティポリシーを統合的に管理するサービス。
- Amazon GuardDuty  
  - 不審なアクティビティを検出するための脅威検出サービス。
- AWS IAM Identity Center (AWS Single Sign-On)  
  - 複数アカウントやアプリケーションへのシングルサインオン（SSO）を提供。
- AWS Identity and Access Management (IAM)  
  - AWSリソースへのアクセスを制御するためのユーザー、グループ、ポリシー管理サービス。
- Amazon Inspector  
  - アプリケーションのセキュリティ評価を自動化するサービス。
- AWS Key Management Service (AWS KMS)  
  - データを保護するための暗号化キーの作成と管理サービス。
- Amazon Macie  
  - 機密データを特定し、保護するためのセキュリティサービス。
- AWS Network Firewall  
  - VPCレベルでのネットワークトラフィックを制御するためのマネージド型ファイアウォール。
- AWS Resource Access Manager (AWS RAM)  
  - 複数のAWSアカウント間でリソースを安全に共有するためのサービス。
- AWS Secrets Manager  
  - パスワードやAPIキーなどの機密情報を安全に管理するためのサービス。
- AWS Security Hub  
  - AWS全体のセキュリティステータスを一元管理するためのダッシュボード。
- AWS Shield  
  - 分散型サービス拒否（DDoS）攻撃からアプリケーションを保護するサービス。
- AWS WAF  
  - アプリケーションを不正アクセスから保護するウェブアプリケーションファイアウォール。

#### **サーバーレス**
- AWS AppSync  
  - GraphQLを使用してサーバーレスアプリケーションを構築し、データソースと接続するサービス。
- AWS Fargate  
  - コンテナのインフラ管理を不要にし、アプリケーションに集中できるサービス。
- AWS Lambda  
  - イベント駆動型でコードを実行するサーバーレスコンピューティングサービス。

#### **ストレージ**
- AWS Backup  
  - AWSリソースのバックアップを統一的に管理し、スケジュール化するサービス。
- Amazon Elastic Block Store (Amazon EBS)  
  - EC2インスタンス用のスケーラブルなブロックストレージ。
- Amazon Elastic File System (Amazon EFS)  
  - Linuxインスタンス向けのスケーラブルな共有ファイルストレージ。
- Amazon FSx (すべてのタイプに対応)  
  - Windows File ServerやLustreなどの特定用途向けファイルシステムを提供するサービス。
- Amazon S3  
  - オブジェクトストレージで、データの保存と取得を可能にするスケーラブルなサービス。
- Amazon S3 Glacier  
  - データアーカイブと長期保存に最適な低コストストレージ。
- AWS Storage Gateway  
  - オンプレミス環境とAWSクラウドを統合するハイブリッドストレージサービス。

---

## 参照文献とか

- [AWS Certified Solutions Architect - Associate (SAA-C03) 試験ガイド](https://d1.awsstatic.com/ja_JP/training-and-certification/docs-sa-assoc/AWS-Certified-Solutions-Architect-Associate_Exam-Guide.pdf)
- [時間がないけどAWS認定試験に合格したい人に贈る効率の良い勉強法 #AWS](https://qiita.com/ozzy3/items/4fb249a77a579a6cbea3)
- [AWS 新資格 Machine Learning Engineer - Associate(MLA-C01)合格体験記](https://qiita.com/ec2_on_aws/items/cc4e245bf47a0d4d803b)
- [AWS認定全冠を維持し続ける理由と12冠(13冠、14冠？)までの学習方法・資格の難易度まとめ －How to become an Japan AWS All Certifications Engineer(formerly known as APN ALL AWS Certifications Engineer)－](https://tech.nri-net.com/entry/all_aws_certifications_engineer)
- [AWS 認定 ソリューションアーキテクト – アソシエイト(AWS Certified Solutions Architect – Associate)の学習方法](https://tech.nri-net.com/entry/aws_certified_solutions_architect_associate)
- 
