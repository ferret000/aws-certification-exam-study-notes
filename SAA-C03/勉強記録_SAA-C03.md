# [勉強記録]AWS Certified Solutions Architect - Associate

## はじめに

- [SAA-C03] 合格に向けた勉強記録をまとめようと思います。
  - 合格したら、Qiita に合格体験記として載せたい ⇒ ギリギリですが、合格できました！
- AWS 資格受験において、どういった問題が出る？等の話は規則としてできないようになっているため、その点は載せていません。
  - [AWS 認定プログラムアグリーメント](https://d1.awsstatic.com/legal/AWS-Certification-Agreement/AWS_Certification_Program_Agreement_Translation_Japanese2.pdf)

## 筆者前提

- SE 歴 10 数年のおじさんです。
- Java 周りのアプリケーションエンジニアがメインでしたが、最近は AWS や Docker を利用した基盤構築をしたりしなかったりしています。
- AWSのサービスだと、下記あたりを業務で触ってました。
  - EC2、ECS、Lambdaあたりのコンピューティング関連
  - S3、EBS、EFSなどのストレージ関連
  - RDB、AuroraなどのDB関連
  - SQS、AmazonMQなどの非同期処理関連
  - CodeファミリーなどのCICD関連
- 逆に、ネットワークやセキュリティ、機械学習、アカウント管理などは全然触っていません。
- この資格取得に向けて勉強するタイミングでは、下記の AWS 認定を取得済です。
  - Foundational
    - [AWS Certified Cloud Practitioner[CLF-C01]](https://aws.amazon.com/jp/certification/certified-cloud-practitioner/?ch=sec&sec=rmg&d=1)
  - Associate
    - [AWS Certified Solutions Architect - Associate](https://aws.amazon.com/jp/certification/certified-solutions-architect-associate/?ch=sec&sec=rmg&d=1) ※失効済
- 今回は過去取得していたが失効した、SSA を再取得するために勉強を始めました。
  - しかも、アカウントを紛失したので過去実績も証明できず・・・

## [SAA-C03] の試験概要

- 試験概要([試験ガイド](https://d1.awsstatic.com/ja_JP/training-and-certification/docs-sa-assoc/AWS-Certified-Solutions-Architect-Associate_Exam-Guide.pdf)を gpt4o で要約)

### **試験概要**

AWS Certified Solutions Architect - Associate (SAA-C03) 試験は、ソリューションアーキテクトを対象とし、AWS Well-Architected フレームワークに基づくソリューション設計能力を評価します。以下のタスクに関する知識とスキルが求められます：

- 現在および将来のビジネス要件に対応する AWS サービスを活用したソリューションの設計。
- 安全性、耐障害性、高パフォーマンス、コスト最適化を実現したアーキテクチャの設計。
- 既存のソリューションのレビューおよび改善提案。

### **試験内容**

- **出題形式**：択一選択問題（正解 1 つ）および複数選択問題（正解 2 つ以上）。
- **問題数**：採点対象問題 50 問、採点対象外問題 15 問（全 65 問）。
- **合否基準**：スコア範囲は 100 ～ 1000 点、合格スコアは 720 点。

### **試験分野と比重**

1. **セキュアなアーキテクチャの設計（30%）**
   - IAM やセキュリティベストプラクティスの活用。
   - セキュアなワークロードおよびデータ管理。
2. **弾力性に優れたアーキテクチャの設計（26%）**
   - スケーラブルかつフォールトトレラントなシステム設計。
3. **高パフォーマンスなアーキテクチャの設計（24%）**
   - ストレージ、コンピューティング、データベース、ネットワークの最適化。
4. **コストを最適化したアーキテクチャの設計（20%）**
   - コスト効率の良いリソース利用と管理。

### **推奨される事前経験**

- AWS サービスを使用した 1 年以上の実務経験。

### **試験対象技術とサービス**

試験範囲に含まれる AWS サービスは、コンピューティング、ストレージ、ネットワーク、データベース、セキュリティ、コスト管理など多岐にわたります。詳細はガイドの付録に記載されています。
※[#Appendix] にまとめています。

## 試験比較(XXX vs YYY)

## 勉強方法

Udemy を中心に学習を進めます。

- AWS Skill Builder デジタルトレーニング
  - AWS Certified Solutions Architect – Associate Official Practice Question Set (SAA-C03 - Japanese)
    - 無料のサンプル問題
  - Exam Prep Standard Course: AWS Certified Solutions Architect - Associate (SAA-C03) (Japanese) 日本語実写版
    - 試験準備のための要点がまとめられているデジタルトレーニング
- Udemy
  - [【SAA-C03 版】AWS 認定ソリューションアーキテクト アソシエイト模擬試験問題集（6 回分 390 問）](https://www.udemy.com/course/aws-knan/?srsltid=AfmBOoroNztq6Qz5jycWJPyYldYoSzxEPPi25ErUVWqyok3liojzo_DQ&couponCode=NEWYEARCAREERJP)
    - 所属会社が Udemy business を契約しており、無料で受講できるものを選定しました。

## 所感

ギリギリですが、なんとか SAA-03 合格できました。（正直落ちたと思ってました）

勉強に掛けられた期間は正味 2 週間くらいで、平日の仕事上がりに喫茶店に寄って２～３時間勉強、くらいです。
休日は家庭にフルコミットしてたので時間を作れませんでしたが、逆に「平日にやらないと勉強時間が無い！」というメリハリがついたのかもしれません。

進め方は前項の通りで、先人の経験の通り時間が無い社会人は、

1. 解説読む
2. 問題解く
3. 間違ったところの解説読む
4. 2~3 をループ

という進め方が良さそうです。次もこの作戦で進めたいと思います。

あと、GitHubに勉強メモをまとめたのも、結果的には良かったです。
Udemyで間違った問題の解説をかいつまんで[**こちら**](SAA-C03_試験範囲内のAWSのサービスと機能.md)にまとめ、通勤の満員電車の中ではひたすらこのメモに目を通していました。
また、iPhoneでこのメモを読み上げさせることで、やる気が湧かない時や移動中でもオーディブルのように耳学習出来て捗った気がします。

ただ今回は、模擬問題の数をこなせなかったので、次受ける試験はもっとサイクル回して自信をもって望みたいと思います。

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

[**こちら**](SAA-C03_試験範囲内のAWSのサービスと機能.md)を参照してください。

---

## 参照文献とか

- [AWS Certified Solutions Architect - Associate (SAA-C03) 試験ガイド](https://d1.awsstatic.com/ja_JP/training-and-certification/docs-sa-assoc/AWS-Certified-Solutions-Architect-Associate_Exam-Guide.pdf)
- [時間がないけど AWS 認定試験に合格したい人に贈る効率の良い勉強法 #AWS](https://qiita.com/ozzy3/items/4fb249a77a579a6cbea3)
- [AWS 新資格 Machine Learning Engineer - Associate(MLA-C01)合格体験記](https://qiita.com/ec2_on_aws/items/cc4e245bf47a0d4d803b)
- [AWS 認定全冠を維持し続ける理由と 12 冠(13 冠、14 冠？)までの学習方法・資格の難易度まとめ －How to become an Japan AWS All Certifications Engineer(formerly known as APN ALL AWS Certifications Engineer)－](https://tech.nri-net.com/entry/all_aws_certifications_engineer)
- [AWS 認定 ソリューションアーキテクト – アソシエイト(AWS Certified Solutions Architect – Associate)の学習方法](https://tech.nri-net.com/entry/aws_certified_solutions_architect_associate)
-
