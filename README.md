# 業務経歴書

<p>（更新中...）</p>


## スキル

基本的にすべて実業務で使用した技術だけを列挙しています。

### 言語

Go  | Python | JavaScript | TypeScript | PHP

### フレームワーク等

Nuxt.js | Pyramid | Vue.js | Laravel

### RDB/NoSQL

MySQL | Redis | PostgreSQL

### クラウド

#### AWS

VPC | S3 | Cloud Front | API Gateway | Lambda | ELB | EC2 | ECS | Fargate | EKS(Kubernetes) | Route53 | IAM | Elasticsearch Service | RDS(MySQL|PostgreSQL) | Aurora | DynamoDB | ElastiCache(Redis) |  SQS | SNS | SES  | Cloud Formation | Cloud Watch | Amazon Personalize | CloudTrail | 


### SaaS/PaaS

GitHub | GitHub Actions | Gitlab | CircleCI | Sentry

### その他

Terraform | Docker  | nginx | Apache | Elasticsearch | IndexedDB

## 主な業務経歴

### 2019年11月〜　不動産紹介支援アプリケーションの開発

#### 【開発作業について】

##### ＜概要＞
　Nuxt.jsとPython（SSR）のアプリケーションの開発・改修に携わっています。主にはバックエンドにて必要なテーブル・APIの作成・修正を行い、それに合わせてフロントの修正も行っています。

##### ＜新規機能開発＞
　Pythonを使ってDB設計やAPI作成を行ったり、それに伴いNuxt.jsでフロント部分の記述を行っていました。DB設計の際には第３正規化まで意識して作業しています。
　バックエンドを中心としながらもフロントも一緒に開発しているため、ユーザーの利便性について考える習慣がついています。

##### ＜KPI＞
　KPIを集計する機能を社内で使用している運営管理画面に作成しました。データベースやRedisから必要な値を取ってきてデータベース上の集計用テーブルに保存するというバッチを定期的に実行する形になっており、月ごと・週ごと・日にち毎の値を表示する仕様になっています。
　ユーザーのアクセスログは、アプリケーションのダッシュボードにて特定のAPIリクエストが投げられると、Redisに一旦保管しておいて、定期的にスクリプトを実行することでその値をRDSの該当テーブルに保存する形になっています。

##### ＜パフォーマンスチューニング＞
　アプリケーションのパフォーマンスチューニングも行いました。バックエンドの処理で、
・forループの中でクエリを書いている場合は、できるだけforループの外でクエリを書く形へと変更。
・外部結合や内部結合を使用して出来るだけクエリを叩く回数を減らす。
・APIリクエストに対してのレスポンスボディで、不要なフィールドが入っているときにその値を取得する処理に時間がかかっていた。そのため新しいシリアライズの形を作るなどして、ネックになっているレスポンスボディのフィールドを減らすように対応。
といった対応を行いました。

##### ＜バグ対応＞
　アプリケーションでエラーが発生している場合は、

・EC2にssh接続してdockerコンテナのログを確認
・Chrome Developer Toolsの NetworkやConsoleを確認
・データベースの値を確認
・ローカル環境にてデバッグ作業
しながら原因を探り作業しています。

　場合によっては、RDSのデータベースのデータをdumpしてローカル環境のデータベースに持ってきて、実際に動かしてログを出力して原因を探ります。ロジック変更に伴い既存のデータの値を変更する必要が出たときにはスクリプトを作成しています。

##### ＜インフラ＞
　AWSのマネジメントサービスを用いたインフラ周りについて、Terraformを用いてコードで管理されており、追加で必要になったEC２やSQSなどを追加・変更することがあります。
　開発作業においてdevelopの環境をもう一つ欲しいという要望があったことからTerraformにて作成しました。

+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

#### 【開発作業以外でのタスク・アクション】
　手を動かしての開発作業と同時に、チームの開発進捗の管理・調整や後輩のサポートなども行なっています。常に開発全体を見て優先順位を見極めながら作業にあたっています。

　営業先の顧客の要望の中で、何にどれくらい時間がかかりそうかというところを一つずつ確認していき、
・次のフェーズまでにどの機能を実装するか
・そのためにどこから取り掛かるか
といった調整を行いました。

　営業の方々の意向で一時期2〜3日ペースで開発を進めていたところを、1〜2週間ペースに切り替えることで営業・開発ともにスケジュールを管理しやすくなるよう提案するなど、業務の改善に繋がる点は提案していました。

　エンジニアの数が少ないこともあり、私が定期的に参加している交流会や勉強会で出会ったエンジニアの方を面接にお誘いするなど、プログラミング以外でも社内の業務環境の向上になることは積極的に取り組んでいます。
　また、社内で定期的に開催されるAWS勉強会にも参加して知識を深め広げ、業務時間外でも学習に積極的に取り組むようにしています。
