---
title: '方法: シンボル情報をシリアル化する | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- VS.ToolsOptionsPages.Performance.General
helpviewer_keywords:
- profiling tools, serializing symbol information
- performance tools, serializing symbol information
ms.assetid: 9e0da706-6325-4073-83d1-aeab3b7c137a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 72a634bd83a55d4e646874cce5546e2a7310afb2
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56617848"
---
# <a name="how-to-serialize-symbol-information"></a>方法: シンボル情報をシリアル化する
アプリケーションの分析に必要なシンボルをシリアル化できます。 シンボルをシリアル化すると、.*vsp* ファイルにシンボルが追加されます。 シンボル情報を .*vsp* ファイルに追加すると、他のユーザーは元のシンボルにアクセスすることなく、パフォーマンス レポートを分析できるようになります。 シンボルがシリアル化されない場合は、元のインストルメント化された .*exe* ファイルおよび .*pdb* ファイルで .*vsp* ファイルを分析する必要があります。

### <a name="to-automatically-serialize-symbol-information"></a>シンボル情報を自動的にシリアル化するには

1.  **[ツール]** メニューの **[オプション]** をクリックします。

     **[オプション]** ダイアログ ボックスが表示されます。

2.  **[パフォーマンス ツール]** をクリックします。

3.  **[全般設定]** で **[シンボル情報を自動的にシリアル化]** を選択します。

## <a name="see-also"></a>関連項目
- [パフォーマンス セッションの構成](../profiling/configuring-performance-sessions.md)
- [方法: Windows シンボル情報を参照する](../profiling/how-to-reference-windows-symbol-information.md)
- [方法: 分析されたレポート ファイルを保存する](/previous-versions/visualstudio/visual-studio-2010/bb763106\(v\=vs.100\))