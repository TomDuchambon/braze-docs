---
nav_title: 非トリガーキャンペーンまたはキャンバス
article_title: 非トリガーキャンペーンまたはキャンバス
page_order: 5

page_type: solution
description: "このヘルプ記事では、キャンペーンまたはキャンバスが予期したとおりにトリガーされない問題を解決するステップについて説明します。"
tool: 
- Campaigns
- Canvas
---

# トリガーを解除したキャンペーンまたはキャンバス

期待されるトリガーの振る舞いを得られなかった理由はいくつかあります。最も一般的なエラーのソリューションは、トリガーしているキャンペーンがSegmentで同じトリガー事象を使用しないようにすることです。

## キャンペーントリガー

セグメントメンバーシップは、トリガーアクションの前に評価されます。つまり、ユーザーが最初にSegmentに入っていなければ、トリガーを実行してもキャンペーンを受信しません。

キャンペーンがカスタムイベントからトリガーされる場合は、このイベントがキャンペーンで使用するセグメントによって事前にフィルタリングされていないことを確認する必要があります。 

例えば、セグメントにイベント `SessionStart` 「アプリを複数回使用した」が含まれており、キャンペーンがトリガーされるイベントが `SessionStart` である場合、ユーザーはメッセージを受信しますが、それが必ずしも最初のセッションのメッセージであるとは限りません。これは、ユーザーがキャンペーンを受信するかどうかを確認する最初のステップ中に、キャンペーンがSegment対象オーディエンスを確認しているためです。 

つまり、オーディエンス フィルターと同じトリガー(変更された属性やカスタムイベントなど)でアクションベースのキャンペーンまたはキャンバスを設定することは避けてください。[競合][2] は、ユーザーがトリガーを実行するときにオーディエンスにない場合に発生することがあります。つまり、キャンペーンを受信したり、キャンバスに入ったりすることはありません。

{% alert tip %}
キャンペーンのトラブルシューティングについては、過去30日分の診断ログしか残っていないため、問題発生から30日以内に必ずBrazeサポートに連絡すること。
{% endalert %}

_最終更新日: 2024年6月25日_

[1]: {{site.baseurl}}/user_guide/data_and_analytics/braze_currents/event_glossary/customer_behavior_events/#session-start-event/
[2]: {{site.baseurl}}/user_guide/engagement_tools/testing/race_conditions/#race-conditions/