---
title: Vsgdbg::vsgdbg (コンス トラクター) |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 670651e6-5e79-4845-b0c2-671beb7055a8
caps.latest.revision: 7
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 056c5f5e19a4d1e025969aa40ad75f3852b4201b
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2018
ms.locfileid: "51781921"
---
# <a name="vsgdbgvsgdbg-constructor"></a>VsgDbg::VsgDbg (コンストラクター)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

指定されたブール値パラメーターに基づいて、既定でグラフィックス情報をアクティブにキャプチャして記録するようにグラフィックス診断のアプリ内コンポーネントを準備をするか、または準備しないで、`VsgDbg` クラスのインスタンスを構築します。  
  
## <a name="syntax"></a>構文  
  
```cpp  
VsgDbg(  
  bDefaultInit  
);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `bDefaultInit`  
 グラフィックス情報をアクティブにキャプチャして記録するように、グラフィックス診断のアプリ内コンポーネントを準備することを指定する場合は `true`、この時点ではグラフィックス情報をアクティブにキャプチャして記録するようにアプリケーションを準備しないことを指定する場合は `false` に設定します。  
  
## <a name="remarks"></a>Remarks  
 コンス トラクターが呼び出された場合`bDefaultInit`に設定`true`、グラフィックス ログ ファイルのファイル名は、方法によって決まります`DONT_SAVE_VSGLOG_TO_TEMP`と`VSG_DEFAULT_RUN_FILENAME`する前にプリプロセッサ シンボルが定義されている`vsgcapture.h`アプリに含まれます。  
  
 `bDefaultInit` が `false` に設定された状態でコンストラクターが呼び出された場合、後で `Init` 関数を呼び出して、グラフィックス情報をアクティブにキャプチャして記録するようにグラフィックス診断のアプリ内コンポーネントを準備できます。  
  
## <a name="see-also"></a>関連項目  
 [VsgDbg:: ~ VsgDbg (デストラクター)](../debugger/vsgdbg-tilde-vsgdbg-destructor.md)   
 [Init](../debugger/init.md)   
 [DONT_SAVE_VSGLOG_TO_TEMP](../debugger/dont-save-vsglog-to-temp.md)   
 [VSG_DEFAULT_RUN_FILENAME](../debugger/vsg-default-run-filename.md)



