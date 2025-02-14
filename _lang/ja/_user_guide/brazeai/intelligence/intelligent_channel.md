---
nav_title: インテリジェントチャネルフィルター
article_title: インテリジェントチャネルフィルター
page_order: 0
description: "この記事では、インテリジェントチャネルフィルターについて説明します。このフィルターは、選択したメッセージングチャネルが最良のチャンネルであるオーディエンスの部分を選択するフィルターです。この場合の最良とは、ユーザーの履歴からエンゲージメントの可能性が最も高い、という意味です。"
search_rank: 11
---

# [![Braze ラーニングコース]({% image_buster /assets/img/bl_icon3.png %})](https://learning.braze.com/most-engaged-channel){: style="float:right;width:120px;border:0;" class="noimgborder"}インテリジェントチャネルフィルター

> インテリジェント、つまり `Most Engaged` チャネルフィルターは、選択したメッセージングチャネルが「最良」のチャネルであるオーディエンス部分を選択します。 

この場合の最良とは、ユーザーの履歴からエンゲージメントの可能性が最も高いチャネルを意味します。メール、SMS、Web プッシュ、またはモバイルプッシュ (利用可能なモバイル OS またはデバイスを含む) をチャネルとして選択できます。

![][1]{: style="float:right;max-width:40%;margin-left:10px;margin-top:10px;border:0"}

インテリジェントチャネルは、3 つのチャネルそれぞれのエンゲージメント率をユーザーごとに計算します。これは、過去 6 か月間に受信したメッセージの数に対する、メッセージのインタラクション数 (開封数またはクリック数) の比率を取得することによって行われます。利用可能なチャネルはそれぞれのエンゲージメント率に応じてランク付けされ、最も比率の高いチャネルがそのユーザーについて「エンゲージメントが最も高い」ことになります。 

メッセージがユーザーに送信されるたびに、またはユーザーがメッセージと対話するたびに、エンゲージメント比率が数秒以内に再計算されます。ユーザーは、メッセージと対話したときに 1 回のみカウントできます (例えば、同じメールを開封してクリックすると、そのメッセージは 2 回ではなく 1 回だけエンゲージされたとマークされます)。 

インテリジェントチャネルフィルターを有効にするには、メール、Web プッシュ、またはモバイルプッシュのキャンペーンの作成時に、[**ターゲットユーザー**] ページで [**インテリジェントチャネル**] フィルターを選択します。

{% alert important %}
SMS チャネルのエンゲージメント率を計算するには、高度な追跡とクリック追跡で [[SMS リンク短縮]({{site.baseurl}}/user_guide/message_building_by_channel/sms/campaign/link_shortening/#overview/)] をオンにします。
{% endalert %}

## 「データ不足」オプション

Braze が「最良」のチャネルを判定するには、十分なデータが必要です。つまり、あるユーザーは、使用可能な 3 つのチャネルのうち少なくとも 2 つを介して 3 件以上のメッセージを受信している必要があります。メッセージは必ずしも開封されている必要はありません。 

ユーザーがこれらのチャネルにわたって十分なメッセージを受信していない場合、それらのユーザーはこのフィルターの [データ不足] オプションに該当します。これにより、3 つの使用可能なメッセージングチャネルのいずれかを使用して、これらのユーザーをターゲットにすることができます。

例えば、プッシュメッセージを好むユーザーにプッシュを受信させ、十分なデータがないユーザーにも同じプッシュメッセージを受信させたいとします。この場合、インテリジェントチャネルフィルターを [**モバイル**] に設定し、[**または**] を使用して、2 番目のインテリジェントチャネルフィルターを [**データ不足**] に設定します。メールを好むユーザーには、インテリジェントチャネルフィルターがメールに設定されている別のキャンペーンで対応できます。

![][2]

{% alert note %}
[フリークエンシーキャップ]({{site.baseurl}}/user_guide/engagement_tools/campaigns/testing_and_more/rate-limiting/#delivery-rules)を無視するキャンペーンとキャンバスステップは、インテリジェントチャネルでは考慮されず、データ要件に貢献できません。
{% endalert %}

## 「モバイルプッシュ」オプション

モバイルプッシュには、Android、iOS、Kindle、および Braze で使用可能なその他のモバイルデバイスチャネルが含まれます。インテリジェントチャネルを計算するときに、Braze は各種類のモバイルデバイスを個別に調べ、その中で最も高いエンゲージメント率を選択して「モバイルプッシュ」カテゴリとし、メールおよび Web プッシュと比較します。 

例えば、あるユーザーが複数のモバイルデバイスを持っている場合、そのモバイルエンゲージメント率は、デバイス全体で最高の率により表されます。しかし、これは、ユーザーがそのデバイス上で排他的にプッシュ通知を受信することを強制しません。この率は、メールおよび Web プッシュと比較する場合にのみ使用されます。

## 個別チャネル

あるユーザーについて単一の最良チャネルを Braze に 選択させるのではなく、選択したチャネルでユーザーがメッセージを開封する確率に基づいて、単にユーザーにフィルターを適用することもできます。そのために、[セグメンテーションフィルター]({{site.baseurl}}/user_guide/engagement_tools/segments/segmentation_filters)でメッセージ開封の可能性フィルターを使用できます。

## ベストプラクティスと効果的な使用の戦略

### 優先判定

一部のユーザーは受信したメッセージ数が少ないため、あるユーザーについて、使用できる複数のチャネルのエンゲージメント率が同じ値になることは珍しくありません (例えば、あるユーザーが、メールとモバイルプッシュの**両方**でエンゲージメント率が 0.2 である場合など)。このような場合、最新の開封イベントを持つチャネルを優先 (より高いランクを付ける) することで、同じ値があっても判定されます。

### 到達不能なチャネル

ランク付けを決定するときにユーザーが十分なデータを持っていても、最もエンゲージメントの高いチャネルで到達不能になった場合、そのユーザーは「脱落」し、メッセージを一切受信しなくなります。特定のチャネルで到達不能なユーザーについては、個別にターゲットにする必要があります。

### オーディエンスのサイズ

インテリジェントチャネルを使用すると、オーディエンスの大部分よりもメッセージにエンゲージする可能性がはるかに高いごく少数のユーザーを、事前に選択してターゲットにすることができます。これは、典型的なオーディエンスに含まれるユーザーの大部分を表すものではありません。むしろ、このフィルターでは、通常のオーディエンスのうち、特定のチャネルでエンゲージメントの実績を持つ 5 ～ 20% のユーザーを見つけられると期待できます。


[1]: {% image_buster /assets/img/intelligent_channel_filter.png %} 「インテリジェントチャネルフィルター」
[2]: {% image_buster /assets/img/intelligent_example.png %}
