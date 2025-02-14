---
nav_title: メールスタイリング
article_title: メールスタイリング
page_order: 2
page_type: reference
description: "この記事では、メールキャンペーンを作成する際に参照するためのメールスタイリングのベストプラクティスを概説します。"
channel: email

---

# メールスタイリング

## アドレススタイリング

**件名**は、受信者がメッセージを受け取ったときに最初に目にするものの一つです。6 ～ 10 語に抑えると、開封率が最も高くなります。 

また、優れた件名を作成するさまざまな手法もあります。読者の関心をそそる質問や、より直接的な件名、また顧客とエンゲージするためのパーソナライゼーションなどです。1 つの件名を使用し続けるのではなく、[AB テスト]({{site.baseurl}}/user_guide/engagement_tools/testing/multivariant_testing/#what-are-multivariate-and-ab-testing/)を活用して、新しい件名を試してその効果を測定します。件名はモバイルで適切に表示されるように35文字以内にする必要があります。

[差出人] フィールドに、送信者を明確に示す必要があります。人の名前や珍しい略語を使わないようにしてください。代わりに、ブランド名のように明確にわかる名前を使用してください。個人名を使用することが、ブランドのメールをパーソナライズする方法に適している場合は、受信者との関係を築けるように一貫性を保ちます。"From" 名はモバイルで適切に表示されるために25文字以内である必要があります。

### 返信不可のアドレス

複数の理由から、返信不可のメールアドレスは一般的に推奨されません。なぜなら、それは読者との関係を断つからです。多くの受信者は購読解除するためにメールに返信します。したがって、それができない場合、たいていは次のアクションとしてメールをスパムとしてマークします。

不在時の返信は実際に貴重な情報を提供し、開封率を高め、スパム報告を減らすことができます（メールを受け取りたくない人を削除することによって）。個人的なレベルでは、返信しないことは受信者に対して非個人的に見える可能性があり、あなたの会社からのさらなるメールの受信を拒否させるかもしれません。

## プレヘッダーのテキスト

メールのプリヘッダーテキストは、メッセージの主旨を効率的に伝えて読者の関心を引き、開封を促すものです。プレヘッダーテキストは、メールマーケターがメールの内容に関する追加情報を提供するためにもよく使用されます。プレヘッダーは、メールの件名の直後に表示されるプレビュー テキストです。次の例では、プレヘッダーは`- Brand. New. Lounge Shorts`です。

![Gmail の受信トレイのプリヘッダーテキスト。「新製品のゆったりした短パン」][61]

表示されるプリヘッダーテキストの量は、ユーザーのメールクライアントとメールの件名行の長さによって異なります。一般的に、メールのプリヘッダーを 50 ～100 文字にすることをお勧めします。

プリヘッダーを書くときに覚えておくべきいくつかのベストプラクティスを示します。

1. アクションへの呼びかけを表示するには、読者にメールを開封してもらわなければなりません。
  - 読者に正しい方向を示しましょう。購読、製品の購入、またはWeb サイトの訪問を促す場合でも。
  - 強い言葉を使って読者にあなたが何を求めているのかを正確に伝えましょう。ただし、それがあなたの会社のブランドボイスを反映していること、そしてすべてのコールトゥアクションが消費者に何らかの価値を示していることを確認してください。
  - プレヘッダーは85文字以内に収め、件名をサポートする説明的なアクションを含める必要があります。

2. メールおよびランディングサイトは、ユーザーがアクセスする際にモバイルに最適化されている必要があります。
  - 隙間広告のボックスがない
  - フォームのフィールドが大きい
  - ナビゲーションが容易
  - テキストが大きい
  - 空白が広い
  - 本文が簡潔
  - 明確なアクションの呼びかけ

### プレヘッダー文字数制限

  |   モバイルメールクライアント  |  制限  |
  |:----------------------:|:-------:|
  | iOS Outlook            | 74      |
  | Androidネイティブ         | 43      |
  | Android Gmail          | 24      |
  | iOSネイティブ             | 82      |
  | iOS Gmail              | 30      |
  {: .reset-td-br-1 .reset-td-br-2 role="presentation" }

  |  デスクトップメールクライアント  |  制限  |
  |:----------------------:|:-------:|
  | Apple Mail             | 33      |
  | Outlook '13            | 38      |
  | Mac用Outlook '15   | 53      |
  | Outlook '16            | 50      |
  {: .reset-td-br-1 .reset-td-br-2 role="presentation" }


  |  Webmail メール クライアント  |  制限  |
  |:----------------------:|:-------:|
  | AOLメール               | 81      |
  | Gmail                  | 119     |
  | Outlook.com            | 49      |
  | Office 365             | 40      |
  | Mail.ru                | 64      |
  {: .reset-td-br-1 .reset-td-br-2 role="presentation" }

## メールのサイズ

必ず、メールのサイズを制限してください。メール本文が 102 KB を超えると、Braze および SendGrid のサーバーに過大な負荷をかけるだけでなく、Gmail やその他のメールクライアントでも切り詰められます。メールのサイズをテキストのみの場合は25KB未満、画像を含む場合は60KB未満に抑えるようにしてください。当社の画像アップローダーを使用して画像をホストし、これらの画像を `href` で参照することを強くお勧めします。

|   テキストのみ   | 画像付きのテキスト |     メールの幅    |
|:-------------:|:----------------:|:------------------:|
| 最大25 KB |   最大60KB   | 最大600ピクセル |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3 role="presentation" }

## テキストの長さ

次の表を参照して推奨されるテキストの長さを確認してください。

| テキスト仕様 | 推奨プロパティ |
| --- | --- |
| 件名の長さ | 最適なモバイル表示のために最大 35 文字 (6 〜 10語) |
| 送信者名の長さ | 最適なモバイル表示のために最大 25 文字 |
| プレヘッダーの長さ | 最大 85 文字 |
{: .reset-td-br-1 .reset-td-br-2 role="presentation" }

## 画像サイズ

推奨される画像サイズについては、次の表を参照してください。小さくて高品質な画像は読み込みが速くなるため、目的の出力を達成するために可能な限り小さいアセットを使用してください。

|     サイズ    | ヘッダー 画像 幅 |  本文の画像の幅  |   ファイルの種類  |
|:-----------:|:------------------:|:------------------:|:-------------:|
| 最大5MB | 最大600ピクセル | 最大480ピクセル | PNG、JPEG、GIF |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3 .reset-td-br-4 role="presentation" }

## ディープリンク

多くのメールはモバイルデバイスで読まれています。[ディープリンク]({{site.baseurl}}/user_guide/personalization_and_dynamic_content/deep_linking_to_in-app_content/)を使用することは、これらのモバイルメール受信者とエンゲージするための優れた方法です。プッシュ通知とアプリ内メッセージを使用すると、ディープリンクはユーザーをアプリ内の指定された送信先に直接連れて行きます。 

しかし、メールでは、受信者がアプリをインストールしているかどうかが明確にわかりません。そのため、ディープリンクを避けることで、アプリを持っていないこれらのメール受信者に対するエラーメッセージを防ぐことができます。

[61]: {% image_buster /assets/img_archive/preheader_example.png %}
