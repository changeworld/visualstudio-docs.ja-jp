---
title: '方法: プロファイル ツールの ETW レポートを作成する | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: bf5547b3-f6c7-4989-9d47-2fe4f1261444
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 310c43ea4dbdf1f50a76b574ec52baa589769034
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56614468"
---
# <a name="how-to-create-a-profiling-tools-etw-report"></a>方法: プロファイリング ツールの ETW レポートを作成する
Windows イベント トレーシング (ETW) レポートには、[!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] プロファイル ツールのパフォーマンス セッションで記録された ETW イベントが一覧表示されます。 ETW データはバイナリ (.*etl*) ファイルで収集されます。 このレポートの詳細については、「[ETW (Event Tracing for Windows) レポート](../profiling/event-tracing-for-windows-etw-report.md)」を参照してください。

> [!NOTE]
>  [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] の場合、インターフェイスに ETW レポートを表示できません。

- [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] のインターフェイスを利用して ETW データを収集する方法については、「[方法:ETW (Event Tracing for Windows) データを収集する](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md)」を参照してください。

- コマンド プロンプトから ETW データを収集する方法については、「[VSPerfCmd](../profiling/vsperfcmd.md)」と「[イベント](../profiling/events-vsperfcmd.md)」を参照してください。

  ETW レポートは **VSReport/summary:etw** コマンドを利用して生成します。 ETW データを含む .*etl* は、プロファイル データ (.*vsp* または .*vsps*) ファイルと同じディレクトリに置く必要があります。 既定では、レポートはコンマ区切り値 (.*csv*) ファイルとして生成されます。 詳細については、「[VSPerfReport](../profiling/vsperfreport.md)」を参照してください。

### <a name="to-generate-an-etw-report"></a>ETW レポートを生成するには

-   **[コマンド プロンプト]** ウィンドウで、次のコマンド ラインを入力します。

     *ToolsPath* **VSPerfReport** *VSPFile*  **/Summary:ETW [/Xml]**

    |||
    |-|-|
    |*ToolsPath*|プロファイリング ツール ユーティリティのパス。 詳細については、「[コマンド ライン ツールへのパスの指定](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md)」をご覧ください。|
    |*VSPFile*|プロファイル データ (.*vsp* または .*vsps*) ファイル。 完全パスまたは部分パスで指定できます。|
    |Xml|XML で書式設定されているレポートを生成します。|
