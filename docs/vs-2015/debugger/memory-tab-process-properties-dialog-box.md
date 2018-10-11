---
title: '[メモリ] タブ、[プロセス プロパティ] ダイアログ ボックス |Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Process properties for Windows NT
ms.assetid: a70785f2-5997-40ec-a90f-80a52449768b
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 45d7933b70555a3c80a094ea8cd3f982e232f5de
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/22/2018
ms.locfileid: "47535247"
---
# <a name="memory-tab-process-properties-dialog-box"></a>[メモリ] タブ ([プロセス プロパティ] ダイアログ ボックス)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

このトピックの最新バージョンをご覧[メモリ] タブの [プロセス プロパティ] ダイアログ ボックス](https://docs.microsoft.com/visualstudio/debugger/memory-tab-process-properties-dialog-box)します。  
  
使用して、**メモリ**タブ プロセスがメモリを使用する方法を説明します。 表示する、[プロセス プロパティ ダイアログ ボックス](../debugger/process-properties-dialog-box.md)、フォーカスを移動、[プロセス ビュー](../debugger/processes-view.md)ウィンドウ。 ツリーで、プロセスの任意のノードを選択し、**プロパティ**から、**ビュー**メニュー。  
  
 次の設定は [使用可能な**メモリ**] タブ。  
  
|入力|説明|  
|-----------|-----------------|  
|**仮想バイト**|プロセスを使用して仮想アドレス空間の現在のサイズ (単位: バイト)。 仮想アドレス空間の使用は、ディスクまたはメイン メモリ ページのいずれかの使用を必ずしも意味しません。 ただし、仮想空間は有限であり、ライブラリを読み込むプロセスの機能を使用して多すぎる制限可能性があります。|  
|**ピーク時の仮想バイト**|プロセスの仮想アドレス空間のバイトの最大数が、いつでも使用されます。|  
|**ワーキング セット**|プロセスのスレッドが最近使用したメモリ ページのセット。 コンピューターの空きメモリのしきい値を超える場合は、ページは、使用されていない場合でも、プロセスのワーキング セットに残されます。 空きメモリがしきい値を下回った場合は、ワーキング セットからページがトリミングされます。 必要な場合は、メイン メモリから出る前にワーキング セットに論理的な障害がなります。|  
|**ピーク ワーキング セット**|任意の時点でこのプロセスのワーキング セット内のページの最大数。|  
|**Pool paged Bytes**|現在のページ プール、プロセスの量が割り当てられます。 ページ プールは、指定されたタスクを実行するときに、オペレーティング システムのコンポーネントが領域を取得する、システム メモリ領域です。 ページ プールのページは、しばらくの間のシステムによってアクセスされない場合、ページング ファイルにページ アウトできます。|  
|**非ページ プールのバイト数**|現在のプロセスによって割り当てられた非ページ プール内のバイト数。 非ページ プールは、取得されたオペレーティング システム コンポーネントによって指定されたタスクを実行するシステム メモリ領域です。 非ページ プールのページをページング ファイルにページ アウトできません。割り当てられている限り、メイン メモリに残ります。|  
|**Private Bytes**|現在のプロセスが割り当てバイト数は、他のプロセスと共有できません。|  
|**空きバイト数**|このプロセスの合計使用されていない仮想アドレス空間。|  
|**予約済みのバイト数**|このプロセスで将来使用するために予約されている仮想メモリの総量。|  
|**空きイメージ容量**|使用されていないか、このプロセス内のイメージで予約されている仮想アドレス空間の量。|  
|**予約イメージ容量**|このプロセス内で実行するイメージによって予約されているすべての仮想メモリの合計。|


