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