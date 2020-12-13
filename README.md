# 職務経歴書

## 主なスキルセット

### 言語

Go | Python | JavaScript | TypeScript | PHP

### フレームワーク等

Nuxt.js | Pyramid | Vue.js | Laravel

### RDB/NoSQL

MySQL | Redis | PostgreSQL

### クラウド

#### AWS

VPC | S3 | CloudFront | API Gateway | Lambda | ELB | EC2 | ECS | Fargate | ECR | Route53 | CloudWatchLogs | IAM | RDS(MySQL|PostgreSQL) | ElastiCache(Redis) | SQS | SES


### SaaS/PaaS

GitHub | GitHub Actions | Gitlab | CircleCI | Sentry

### その他

Terraform | Docker | nginx | Apache | Serverless Framework


## 主な業務経歴

### ①2019年11月〜　不動産紹介支援アプリケーションの開発 (Python/Nuxt.js)

#### 【開発作業について】

##### ＜概要＞
　Nuxt.jsとPython（SSR）のアプリケーションの開発・改修に携わっています。主にはバックエンドにて必要なテーブル・APIの作成・修正などを行い、Terraformを用いたインフラ管理やフロントの作成・修正も行っています。

##### ＜ECSでのコンテナ管理を導入＞
　本番環境にて、EC2インスタンスの中でDocker-composeでコンテナを管理していたところを、ECSを用いたコンテナ管理へと変更。
Terraformを使用してコードでリソースの追加・変更を実行。本番以外の環境（develop環境・Stage環境）で本番とほぼ同じ環境を構築して検証を重ねたうえで、本番環境にて実行しました。

##### ＜KPI＞
　KPIを集計する機能を社内で使用している運営管理画面に作成しました。データベースやRedisから必要な値を取ってきてデータベース上の集計用テーブルに保存するというバッチを定期的に実行する形になっており、月ごと・週ごと・日にち毎の値を表示する仕様になっています。
　ユーザーのアクセスログは、アプリケーションのダッシュボードにて特定のAPIリクエストが投げられると、Redisに一旦保管しておいて、定期的にスクリプトを実行することでその値をRDSの該当テーブルに保存する形になっています。

##### ＜パフォーマンスチューニング＞
　アプリケーションのパフォーマンスチューニングも行いました。バックエンドの処理で、
 <ul>
<li>forループの中でクエリを書いている場合は、できるだけforループの外でクエリを書く形へと変更。</li>
<li>外部結合や内部結合を使用して出来るだけクエリを叩く回数を減らす。</li>
<li>APIリクエストに対してのレスポンスボディで、不要なフィールドが入っているときにその値を取得する処理に時間がかかっていた。そのため新しいシリアライズの形を作るなどして、ネックになっているレスポンスボディのフィールドを減らすように対応。</li>
</ul>
といった対応を行いました。

##### ＜新規機能開発＞
　Pythonを使ってDB設計やAPI作成を行ったり、それに伴いNuxt.jsでフロント部分の記述を行っていました。DB設計の際には第３正規化まで意識して作業しています。
　バックエンドを中心としながらもフロントも一緒に開発しているため、ユーザーの利便性について考えるよう意識しています。

##### ＜バグ対応＞
　アプリケーションでバグが発生している場合は、
<ul>
<li>CloudWatchLogsのログを確認</li>
<li>Chrome Developer Toolsの NetworkやConsoleなどを確認</li>
<li>データベースの値を確認</li>
<li>ローカル環境にてデバッグ作業</li>
</ul>
といった作業を通じて原因を探ります。

　場合によっては、RDSのデータベースのデータをdumpしてローカル環境のデータベースに持ってきて、実際に動かしてログを出力して原因を探ります。ロジック変更に伴い既存のデータの値を変更する必要が出たときにはスクリプトを作成しています。

##### ＜インフラ＞
　AWSのマネジメントサービスを用いたインフラ周りについて、Terraformを用いてコードで管理されており、追加で必要になったEC２やSQSなどを追加・変更することがあります。
　開発作業においてdevelopの環境をもう一つ欲しいという要望があったことからTerraformにて作成しました。

【主な使用技術】
<ul>
 <li>Python 3.7.5</li>
 <li>Nuxt.js 2.11</li>
 <li>TypeScript 3.9</li>
 <li>AWS</li>
 <li>VPC</li>
 <li>EC2</li>
 <li>Route53</li>
 <li>RDS for MySQL</li>
 <li>ElastiCache(Redis)</li>
 <li>S3</li>
 <li>ALB</li>
 <li>ECS</li>
 <li>ECR</li>
 <li>Terraform</li>
 <li>AWS Secrets Manager</li>
 <li>Docker</li>
 <li>Severless Framework</li>
 <li>API Gateway</li>
 <li>Lambda</li>
 <li>CloudWatchLogs</li>
</ul>

=============================================================================

#### 【開発作業以外でのタスク・アクション】
　手を動かしての開発作業と同時に、チームリーダーという役割も担っており、チームの開発進捗の管理・調整や後輩のサポートなども行なっています。常に開発全体を見て優先順位を見極めながら作業にあたっています。

　営業先の顧客の要望の中で、何にどれくらい時間がかかりそうかというところを一つずつ確認していき、
<ul>
<li>次のフェーズまでにどの機能を実装するか</li>
<li>そのためにどこから取り掛かるか</li>
</ul>

といった調整を行いました。

　営業の方々の意向で一時期2〜3日ペースで開発を進めていたところを、1〜2週間ペースに切り替えることで営業・開発ともにスケジュールを管理しやすくなるよう提案するなど、業務の改善に繋がる点は提案していました。

　エンジニアの数が少ないこともあり、私が定期的に参加している交流会や勉強会で出会ったエンジニアの方を面接にお誘いするなど、プログラミング以外でも社内の業務環境の向上になることは積極的に取り組んでいます。
　また、社内で定期的に開催されるAWS勉強会にも参加して知識を深め広げ、業務時間外でも学習に積極的に取り組むようにしています。

----------------------------------------------------------------------------------------------------

### ②2020年４月〜　オリジナルのアプリケーション開発(Golang/Nuxt.js/AWS)

　プライベートの時間で開発しているGolang + Nuxt.jsのアプリケーションです。アプリケーション（PHP/Laravel+Nuxt.jsのSPA）のバックエンドをGolangにリプレイスしました。
　Spotifyの無料アカウントを作ってお持ちであれば、Spotifyで曲を検索して投稿することができます。
  実際に業務でGolangを使用している方に、コードレビューしてもらいながら実装を進めています。

【アプリケーションURL】
http://your-songs-laravel.site

【Github】
アプリケーションの詳細は以下のGithubリポジトリから確認できます。
<ul>
<li>https://github.com/kt-321/golang-songs　→　Golang</li>
<li>https://github.com/kt-321/nuxt-songs-go　→　Nuxt.js</li>
</ul>
　
【主な使用技術】
<ul>
 <li>Golang 1.14</li>
 <li>Nuxt.js 2.11</li>
 <li>TypeScript 3.9</li>
 <li>AWS</li>
 <li>VPC</li>
 <li>EC2</li>
 <li>Route53</li>
 <li>RDS for MySQL</li>
 <li>ElastiCache(Redis)</li>
 <li>S3</li>
 <li>ALB</li>
 <li>ECS</li>
 <li>ECR</li>
 <li>Terraform</li>
 <li>AWS Secrets Manager</li>
</ul>

【Golangのコード】
<ul>
 <li>net/httpパッケージでHTTPサーバーの起動</li>
 <li>gorilla/muxを用いてルーティング作成</li>
 <li>ORM用ライブラリGORMを使用</li>
 <li>sql-migrateを用いてマイグレーション</li>
 <li>パッケージ管理にGOMODULE使用</li>
 <li>testingパッケージを用いてテストコード記述</li>
 <li>go-jwt-middlewareパッケージを用いてJWT認証の実装</li>
 <li>Redigoを用いてRedisの使用</li>
 <li>HTTPサーバーのgraceful shutdown</li>
 <li>encoding/jsonを用いてjsonのエンコード/デコード</li>
 <li>bcryptを用いてパスワードをハッシュ化</li>
 <li>GolangCI-Lintの使用</li>
 <li>デバッグにdelveを使用</li>
</ul>

構造体にjsonタグを付与することで、APIリクエストがあるとJSON形式でフロントにレスポンスを返しています。

【実装済みの主な機能】
<ul>
 <li>ユーザー登録・ログイン</li>
 <li>ユーザー情報の取得</li>
 <li>ユーザー情報編集</li>
 <li>SpotifyAPIを用いた曲検索</li>
 <li>曲の追加</li>
 <li>曲情報の取得</li>
 <li>曲の編集</li>
 <li>曲の削除</li>
 <li>曲をお気に入りする機能</li>
 <li>曲の絞り込み</li>
 <li>Redis(ElastiCache)の（曲の取得・追加・更新・削除）</li>
 <li>多層キャッシュ構造</li>
 <li>Clean Architectureを倣ったディレクトリ構成</li>
 <li>テストコード</li>
 <li>Github Actionsを用いた自動テスト</li>
 <li>Github Actionsを用いて、ECR へのimageの自動push, ECS(Fargate)でのコンテナ作成</li>
</ul>



【現在実装中】
<ul>
<li>画像をアップロードしてS3に保存する機能</li>
<li>CloudFrontの導入</li>
<li>Lambda・API Gatewayの導入</li>
</ul>

----------------------------------------------------------------------------------------------------

### ③2018年4月〜　中国電力株式会社で法人営業として勤務

法人営業として勤め、電気の大口のお客様を相手に営業活動・契約の締結が主な業務内容でした。
業務の効率化に繋がることについては意見を述べるように心がけていました。
