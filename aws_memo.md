# AWS memo

- AWSアカウントの作成
    - 住所が英語なのでメンドイ

- SNS (SimpleNotificationService)
    - トピック作成。
    - CloudWatchのアラーム用。自分のメールアドレスを登録。

- CloudWatch
    - アラームを追加したり、ログ出力したり色々な監視ができるっぽい。
    - 利用料金が0円を超えた場合にメール通知するよう設定。
    
- IAM (Identity and Access Management)
    - アクセス権とか設定できる。
    - ルートアカウント(AWSアカウント)のMFA(二段階認証)有効化。
    - 管理用IAMユーザー作成。請求関連(Billing)の閲覧はAWSアカウントのみ。
    - グループ作成。
    - パスワードポリシー適用。

- S3 (Simple Storage Service)
    - バケット作成。 (azuma-work)
    - オブジェクトにcreate-react-appのbuildフォルダアップロード。  
    →静的ホスティングの設定をしてブラウザで表示確認。

- AWSCLIのhistory設定
    - 今後の勉強のために、awscliで実行したコマンド履歴を見れるように設定。
    - 初期設定
        ```
        $ aws configure set cli_history enabled

        $ cat ~/.aws/config 
        [default]
        region = ap-northeast-1
        output = json
        cli_history = enabled       # これが追加されていればOK
        ```
    - 一覧表示
        ```
        $ aws history list
        7bd6883c-a8ff-407c-8f45-bb7d29c22a45  2020-03-12 12:29:29 PM  s3 ls                                             0
        67e3374f-1c79-4a7b-a9cd-d67f26a0a481  2020-03-12 12:23:49 PM  iam list-access-keys                              255
        bc4f6584-be4b-45d3-a87a-301d90b9737e  2020-03-12 12:23:01 PM  iam list-account-aliases                          255
        ```
    - 詳細表示
        ```
        $ aws history show
        ```
        もしくはID指定して
        ```
        $ aws history show 7bd6883c-a8ff-407c-8f45-bb7d29c22a45
        ```