---
title: '方法: プロファイリング ツールの ETW レポートを作成する | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: bf5547b3-f6c7-4989-9d47-2fe4f1261444
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: e8ad32f3231915c86f9578563ec4c0684435a3ee
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54797338"
---
# <a name="how-to-create-a-profiling-tools-etw-report"></a>方法: プロファイリング ツールの ETW レポートを作成する
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Windows イベント トレーシング (ETW) レポートには、[!INCLUDE[vsprvs](../includes/vsprvs-md.md)] プロファイル ツールのパフォーマンス セッションで記録された ETW イベントが一覧表示されます。 ETW データはバイナリ (.etl) ファイルで収集されます。 このレポートの詳細については、「[ETW (Event Tracing for Windows) レポート](../profiling/event-tracing-for-windows-etw-report.md)」を参照してください。  
  
> [!NOTE]
>  [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] の場合、インターフェイスに ETW レポートを表示できません。  
  
- [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] のインターフェイスを利用して ETW データを収集する方法については、「[方法: ETW (Event Tracing for Windows) データを収集する](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md)」を参照してください。  
  
- コマンド プロンプトから ETW データを収集する方法については、「[VSPerfCmd](../profiling/vsperfcmd.md)」と「[イベント](../profiling/events-vsperfcmd.md)」を参照してください。  
  
  ETW レポートは **VSReport/summary:etw** コマンドを利用して生成します。 ETW データを含む .etl は、プロファイル データ (.vsp または .vsps) ファイルと同じディレクトリに置く必要があります。 既定では、レポートはコンマ区切り値 (.csv) ファイルとして生成されます。 詳細については、「[VSPerfReport](../profiling/vsperfreport.md)」を参照してください。  
  
### <a name="to-generate-an-etw-report"></a>ETW レポートを生成するには  
  
-   **[コマンド プロンプト]** ウィンドウで、次のコマンド ラインを入力します。  
  
     *ToolsPath* **VSPerfReport** *VSPFile*  **/Summary:ETW [/Xml]**  
  
    |||  
    |-|-|  
    |*ToolsPath*|プロファイリング ツール ユーティリティのパス。 詳細については、「[コマンド ライン ツールへのパスの指定](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md)」をご覧ください。|  
    |*VSPFile*|プロファイル データ (.vsp または .vsps) ファイル。 完全パスまたは部分パスで指定できます。|  
    |Xml|XML で書式設定されているレポートを生成します。|
