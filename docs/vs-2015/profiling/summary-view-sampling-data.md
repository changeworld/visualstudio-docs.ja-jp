---
title: 概要ビュー - サンプリング データ | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- sampling profiling method, Summary view
- Summary view
ms.assetid: 79056873-2985-40be-9112-cdbc26a65156
caps.latest.revision: 18
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 8570692ec620ee50cd24f3fa95ceec8b21172919
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/19/2019
ms.locfileid: "54803086"
---
# <a name="summary-view---sampling-data"></a>概要ビュー - サンプリング データ
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

概要ビューでは、プロファイリング実行で最もパフォーマンス負荷の高い関数についての情報を表示します。 通知リンクとレポート リストの説明など詳細については、「[Summary View](../profiling/summary-view.md) (概要ビュー)」をご覧ください。  
  
> [!NOTE]
>  Windows 8 および Windows Server 2012 の強化されたセキュリティ機能によって、Visual Studio プロファイラーがこれらのプラットフォームでデータを収集する方法に大幅な変更が必要になりました。 Windows ストア アプリにも新しい収集手法が必要です。 「[Windows 8 および Windows Server 2012 アプリケーションのパフォーマンス ツール](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md)」を参照してください。  
  
## <a name="timeline-graph"></a>タイムライン グラフ  
 [概要] ビューのタイムライン グラフには、プロファイリングが行われた期間中のプロファイリング対象アプリケーションのプロセッサ (CPU) 使用率が表示されます。 タイムライン グラフを使用すると、選択した期間に対してフィルター処理した結果を表示できます。 詳細については、「[How to: Filter Report Views from the Summary Timeline](../profiling/how-to-filter-report-views-from-the-summary-timeline.md) (方法: 概要ビューのタイムラインからレポート ビューをフィルター処理する)」をご覧ください。  
  
## <a name="hot-path"></a>ホット パス  
 **[ホット パス]** には、大部分のサンプルが収集された実行パスが表示されます。 関数をクリックすると、その関数の [関数の詳細] ビューが表示されます。 関数のその他のビューを表示するには、関数を右クリックし、一覧からビューをクリックします。  
  
 **[ホット パス]** には、関数ごとに次のデータが含まれています。  
  
|Column|説明|  
|------------|-----------------|  
|**Name**|関数の名前。|  
|**包括サンプル %**|この関数またはこの関数によって呼び出された関数を実行したときに発生したすべてのサンプルの割合。|  
|**排他サンプル %**|この関数が関数本体のコードを実行していたときに発生したすべてのサンプルの割合。 この関数によって呼び出された関数で収集されたサンプルは含まれません。|  
  
## <a name="functions-doing-most-individual-work"></a>最も頻繁に個別の作業を実行している関数  
 **[最も頻繁に個別の作業を実行している関数]** リストには、プロファイリング実行で排他サンプル数が最大の関数が表示されます。 排他サンプルは、サンプルの収集時に、関数が独自のコードを実行している場合に、関数に割り当てられます。 排他サンプルは、サンプルの収集時に、関数が別の関数を呼び出している場合は、関数に割り当てられません。 排他サンプルの数が多いということは、関数自体で膨大な時間が費やされたことを示します。  
  
 関数をクリックすると、その関数の [関数の詳細] ビューが表示されます。 関数のその他のビューを表示するには、関数を右クリックし、一覧からビューをクリックします。  
  
 **[最も頻繁に個別の作業を実行している関数]** には、関数ごとに次のデータが含まれています。  
  
|Column|説明|  
|------------|-----------------|  
|**Name**|関数の名前。|  
|**サンプル % (関数のみ)**|この関数が関数本体のコードを実行していたときに収集された、プロファイリング実行内のすべてのサンプルの割合。 この関数から呼び出された関数が実行されていたときに収集されたサンプルは除外されます。|  
  
## <a name="see-also"></a>関連項目  
 [概要ビュー](../profiling/summary-view-dotnet-memory-data.md)   
 [概要 ビュー](../profiling/summary-view-instrumentation-data.md)
