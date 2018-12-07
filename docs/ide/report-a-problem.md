---
title: '概要: Visual Studio での問題を報告する'
description: 問題の報告ツールの概要および問題の状態と定義について説明します
ms.date: 11/15/2018
ms.prod: visual-studio-dev15
ms.technology: vs-acquisition
ms.topic: conceptual
author: seaniyer
ms.author: seiyer
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 56047150ce98cb6554248e43b7b8d7ff433cf283
ms.sourcegitcommit: 331dbb12e11fcd7f5d15fab05f3c861e48126e43
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2018
ms.locfileid: "51826675"
---
# <a name="overview-report-a-problem"></a>概要: 問題を報告する

Visual Studio 開発者コミュニティは、問題の報告ツールを使用することで、問題を送信することができます。 個々の問題報告が、コア エンジニアリング システムでの作業項目になり、製品チームと直接協力して、影響の大きい問題を識別し、解決することができます。 お客様から送られてくる多くの診断情報を含むフィードバックは、Visual Studio 製品ファミリの向上に不可欠です。 問題の報告に時間を割いていただいて本当に感謝いたします。

さらに、他のコミュニティ メンバーからのフィードバックに投票して、問題がいっそう注目されるようにすることで、より迅速な修正を支援できます。

## <a name="problem-status"></a>問題の状態

問題を報告した後は、提出した問題がライフサイクルのどの段階にあるかが状態で示されます。 Microsoft のチームがフィードバックを検討して、適切な状態に設定します。  以下で意味と色を示すインジケーターを参照することで、問題の報告の進行状況を追跡できます。

![開発者コミュニティでの問題報告の "新規" 状態](../ide/media/ProblemStates/New.jpg)

**[新規]** は、バグまたは問題が新しく報告されたものであり、アクションはまだ実行されていないことを示します。

- - -

![開発者コミュニティでの問題報告の "トリアージ済み" 状態](../ide/media/ProblemStates/Triaged.jpg)

**[トリアージ済み]** は、モデレート、翻訳、重複の初期確認などの準備作業が完了していることを示します。 チケットは、検討のために適切なエンジニア リング チームに送られています。

- - -

![開発者コミュニティでの問題報告の "検討中" 状態](../ide/media/ProblemStates/UnderConsideration.jpg)

**[検討中]** は、Microsoft が問題のコミュニティへの影響を確認しており、それに従って優先順位が設定されることを示します。 コミュニティへの影響が明らかではないか、まだ重大ではない場合、問題はこの状態で監視を継続されます。

- - -

![開発者コミュニティでの問題報告の "調査中" 状態](../ide/media/ProblemStates/UnderInvestigation.jpg)

**[調査中]** は、エンジニアが問題の解決策を積極的に調査していることを示します。

- - -

![開発者コミュニティでの問題報告の "さらに情報が必要です" 状態](../ide/media/ProblemStates/NeedMoreInfo.jpg)

**[さらに情報が必要です]** は、調査を進めるには、お客様からさらに診断情報が必要であることを示します。  [詳細情報の要求への応答方法についてはこちらをご覧ください](./how-to-report-a-problem-with-visual-studio-2017.md#when-further-information-is-needed-need-more-info)。

- - -

![開発者コミュニティでの問題報告の "修正済み - リリース保留中" 状態](../ide/media/ProblemStates/FixedPendingRelease.jpg)

**[修正済み - リリース保留中]** は、問題の修正プログラムができており、次回のプレビューまたはリリースで使用できることを示します。  修正プログラムがプレビューで利用可能になると、プレビュー バージョンを指定する "修正済み" タグが問題に付けられます。

- - -

![開発者コミュニティでの問題報告の "クローズ - 修正済み" 状態](../ide/media/ProblemStates/ClosedFixed.jpg) 

**[クローズ - 修正済み]** は、問題の修正プログラムがリリースされたことを示します。 問題にも、リリース バージョンを指定する "修正済み:" タグが付けられます。

- - -

![開発者コミュニティでの問題報告の "クローズ - 重複" 状態](../ide/media/ProblemStates/ClosedDuplicate.jpg)

**[クローズ - 重複]** は、問題が別のフィードバックで既に報告されていることを示します。 元の問題の報告を追跡できるリンクが提供されます。

- - -

![開発者コミュニティでの問題報告の "終了 - 優先度が低い" 状態](../ide/media/ProblemStates/ClosedLowerPriority.jpg)

**[終了 - 優先度が低い]** 開発者コミュニティの各メンバーに最高の価値を提供することに集中するため、お客様への影響が高い問題から優先順位を設定します。 現時点ではこの特定の問題に対処できませんが、すべてのフィードバックが貴重であり Visual Studio の向上に役立つものと確信しています。

- - -

![開発者コミュニティでの問題報告の "クローズ - バグではない" 状態](../ide/media/ProblemStates/ClosedNotaBug.jpg)

**[クローズ - バグではない]** は、報告された機能が現在の設計であると判断されたことを示します。

- - -

![開発者コミュニティでの問題報告の "終了 - 情報が不十分" 状態](../ide/media/ProblemStates/ClosedNotEnoughInfo.jpg)

**[終了 - 情報が不十分]** は、これを調査するのに十分な情報がないことを示します。 必要な情報が得られた後で、フィードバックを再検討いたします。

- - -

![開発者コミュニティでの問題報告の "終了 - 他の製品" 状態](../ide/media/ProblemStates/ClosedOtherProduct.jpg)

**[終了 - 他の製品]** は、問題が別の製品に適用されると判断されたことを示します。 外部の製品および関連するリンクについては、Microsoft からのコメントを参照してください。

- - -

![開発者コミュニティでの問題報告の "クローズ - 修正できない" 状態](../ide/media/ProblemStates/ClosedWontFix.jpg)

**[クローズ - 修正できない]** は、製品の方向性との整合またはコミュニティへの影響がないなどの要因により、この問題の追求は行われないことを示します。 詳細については、Microsoft からのコメントを参照してください。  この特定の問題には対処できませんが、すべてのフィードバックが貴重であり Visual Studio の向上に役立つものと確信しています。

- - -

## <a name="faq"></a>FAQ

### <a name="how-can-i-increase-the-chance-of-my-problem-getting-resolved-quickly"></a>問題が迅速に解決される可能性を高くするにはどうすればよいですか。

検索を使用して、既に報告された問題を報告しようとしていないことを確認することをお勧めします。 ご自分の問題と一致する既存の項目が見つかった場合は、その問題チケットに投票します。

 私どものチームが発生していることを再現するのに役立つすべての情報を提供してください。  この情報には、必要な再現手順、コード フラグメント、スクリーンショット、再現の記録、ログ ファイル、その他の成果物が含まれます。  「[Visual Studio で問題を報告する方法](./how-to-report-a-problem-with-visual-studio-2017.md)」をご覧ください。

### <a name="how-is-my-feedback-prioritized"></a>フィードバックの優先順位付けはどのように行われるのですか。

お客様からは多くの貴重な問題が送られてきます。 開発者コミュニティの各メンバーに最高の価値を提供できるよう、フィードバックへのアクションには、コミュニティへの影響が大きいものから優先順位を付けます。

お客様のフィードバックに個人的にお答えできない場合でも、報告を十分に理解していることをご承知ください。 すべてのフィードバックは適切なチームに確実に手渡されます。

お客様が Visual Studio をより良くするために費やされた時間に感謝いたします。

### <a name="what-actions-can-i-take-if-im-not-satisfied-with-the-resolution"></a>解決策に満足できない場合は、どのようなアクションを実行できますですか。

私どものチームはお客様が経験された問題の診断と修正に最善を尽くしますが、私どもがお勧めすることにお客様が完全には満足されないこともあります。 フィードバックでコメントを戻し、満足できない点について正確にお知らせいただけば、可能な限りニーズを満たすよう努めます。

### <a name="how-will-i-get-notified-of-progress-on-my-feedback"></a>フィードバックについての進捗状況はどのように通知されますか。

Microsoft のエンジニア リング チームは、フィードバック チケットにコメントし、進捗があったときはチケットの状態を変更することによって、お知らせします。 チケットの状態が変化したとき、またはコメントが投稿されたときに送信されるメール通知にご注意ください。  開発者コミュニティ サイトでのプロファイル設定とユーザー設定により、通知の頻度を管理することができます。

### <a name="why-cant-i-add-a-problem-for-visual-studio-ide-on-the-developer-community-website"></a>開発者コミュニティ Web サイトで Visual Studio IDE に対する問題を追加できないのはなぜですか。

Visual Studio を使用して問題を報告すると、レポートに自動的に診断情報を含めることができます。 それは、問題を完全に理解して解決するために必要なコンテキストを私どものエンジニアに提供する重要な情報です。

Visual Studio を使用して報告すると、大量のログ ファイル、クラッシュ情報、スクリーンショット、再現記録、および高品質の解決策を迅速にお客様に適用するのに役立つ他の成果物など、豊富な診断情報を私どもと簡単に共有できます。