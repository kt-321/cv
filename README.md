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

Terraform | Docker | nginx | Apache | Serverless Framework<br><br><br>


## 主な業務経歴

### ①2019年11月〜　不動産紹介支援アプリケーションの開発 (Python/Nuxt.js)

#### 【開発作業について】

##### 【概要】
　Nuxt.jsとPython（SSR）のアプリケーションの開発・改修に携わっています。主にはバックエンドにて必要なテーブル・APIの作成・修正などを行い、Terraformを用いたインフラ管理やフロントの作成・修正も行っています。

##### 【これまでの主な業務内容】
##### ＜ECSでのコンテナ管理を導入＞
　本番環境にて、EC2インスタンスの中でDocker-composeでコンテナを管理していたところを、ECSを用いたコンテナ管理へと変更。<br>　Terraformを使用してコードでリソースの追加・変更を実行。本番以外の環境（Develop環境・Stage環境）で本番とほぼ同じ環境を構築して検証を重ねたうえで、本番環境にて実行しました。

##### ＜KPI＞
　KPIを集計する機能を社内で使用している運営管理画面に作成しました。バッチを準備して、RDSやRedis(ElastiCache)から必要な値を取ってきて、RDSに用意した集計用テーブルに保存しています。<br>　管理画面からGetAPIを叩くことで、RDSのリードレプリカから月・週・日ごとの値を取得して表示する仕様になっています。

##### ＜パフォーマンスチューニング＞
　パフォーマンスチューニングを行いました。バックエンドの処理で、
 <ul>
<li>クエリは出来るだけforループの外で記述するように変更。</li>
<li>結合を使用して出来るだけクエリを叩く回数を減らす。</li>
<li>APIリクエストに対してのレスポンスボディで、不要なフィールドが入っているときにその値を取得する処理に時間がかかっていた。そのため新しいシリアライズの形を作るなどして、ネックになっているレスポンスボディのフィールドを減らすように対応。</li>
</ul>
<br>などの対応を行いました。

##### ＜新規機能開発＞
　Pythonを使ってDB設計やAPI作成を行ったり、それに伴いNuxt.jsでフロントエンドの記述も行います。<br>　バックエンドを中心としながらもフロントも一緒に開発しているため、ユーザーの利便性について考えるよう意識しています。<br>　複数SQL文を使う時はトランザクション制御を意識しています。

##### ＜バグ対応＞
　アプリケーションでバグが発生している場合は、
<ul>
<li>CloudWatchLogsのログや、データベースの値などを確認</li>
<li>APIのレスポンスを確認し、フロントエンドでの問題かバックエンドの問題かの切り分け</li>
<li>デバッガを用いたデバッグ作業</li>
</ul>
などの手順を踏みながら原因を探ります。<br>　場合によっては、RDSのデータをdumpしてローカル環境に持ってきて原因を探ります。<br>　既存のデータの値を変更する必要が出たときにはスクリプトを作成しています。

##### ＜インフラ周り＞
　AWSのマネジメントサービスを用いたインフラ周りについて、Terraformを用いてコードで管理されており、リソースを追加・変更することがあります。<br>　開発作業において検証用の環境を追加で一つ欲しいという要望があったことからTerraformにて作成しました。
 
##### ＜Docker＞
　（ECSへの以降前に）EC2上に立ち上げられているDockerコンテナをDocker Composeを用いて管理。新規に追加・停止・名前変更などの対応を行いました。<br><br>

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
<br><br>
#### 【開発作業以外でのタスク・アクション】
　手を動かしての開発作業と同時に、チームリーダーという役割も担っており、常に開発全体および営業の要望を確認しながら優先順位を決めて作業にあたっています。<br><br>　営業の要望の中で、どこにどれくらい時間がかかりそうかをissue単位で見積もりしていき、
<ul>
<li>次のフェーズまでにどの機能を実装するか</li>
<li>そのためにどこから取り掛かるか</li>
<li>リリース完了までの進捗報告</li>
</ul>
といった調整を行いました。<br>　社内のエンジニアの数が多くないこともあり、私が定期的に参加している交流会や勉強会で出会ったエンジニアの方を面接にお誘いするなど、社外でも会社のためになることは積極的に取り組みました。<br>　また、交流会や知り合いのエンジニアとの集まりなどに積極的に参加して、様々なエンジニアの方とお話しすることで知見を得たり視野を広げることに繋げています。

----------------------------------------------------------------------------------------------------
<br><br>
### ②2020年４月〜　オリジナルのアプリケーション開発(Golang/Nuxt.js/AWS)

　Golang + Nuxt.jsおよびAWSで開発しているアプリケーションです。アプリケーション（PHP/Laravel+Nuxt.jsのSPA）のバックエンドをGolangにリプレイスしました。<br>　Spotifyの無料アカウントを作ってお持ちであれば、Spotifyで曲を検索して投稿することができます。<br>　実際に業務でGolangを使用している方に、コードレビューしてもらいながら実装を進めています。

【アプリケーションURL】<br>　http://your-songs-laravel.site

【Github】<br>　アプリケーションの詳細は以下のGithubリポジトリから確認できます。
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

<br><br>【Golangのコード】
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

<br><br>【実装済みの主な機能】
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

<br><br>【実装予定】
<ul>
<li>画像をアップロードしてS3に保存する機能</li>
<li>CloudFrontの導入</li>
<li>Lambda・API Gatewayの導入</li>
</ul>

----------------------------------------------------------------------------------------------------
<br>
### ③2018年4月〜　中国電力株式会社で法人営業として勤務<br><br>　法人営業として勤め、電力の大口のお客様を相手に営業活動・契約の締結が主な業務内容でした。<br>　多角的な視点での課題解決能力・与えられたタスク以外にも積極的に取り組むという点を評価していただき、業務に携わっていました。<br>　業務の効率化に繋がることについては積極的に意見を述べるように心がけていました。
