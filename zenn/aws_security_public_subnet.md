## 前提
ALB, EC2

## 疑問
普通EC2はプライベートサブネットに置くらしいけど、パブリックサブネットに置いてもセキュリティグループのインバウンドをALBからのみ許可すればいいのでは？そうすれば、時間料金+データ転送量料金がかかってしまうNAT Gatewayを使わずに済む。

## 余談
[AWS Startup Loft Tokyo](https://aws-startup-lofts.com/apj/loft/tokyo)内の「Ask An Expert」で、直接社員さんに伺いました。ここに行けばほぼいつでも社員さんに質問することができます。

## 結論
セキュリティグループの設定を間違えなければ問題ない。しかし、設定ミスや権限付与のミス、アクセスキーの漏えい等の可能性が0ではない以上、プライベートサブネットに配置するほうが望ましい。
私は、とりあえず開発環境ではありなのかなと思いました。アクセスキー等ハードコーディングしないよう気を付けましょう。

