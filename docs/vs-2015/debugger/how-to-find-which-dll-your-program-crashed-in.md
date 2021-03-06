---
title: '方法: プログラム クラッシュが発生している DLL 確認 |Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.dll
dev_langs:
- FSharp
- VB
- CSharp
- C++
- VB
- CSharp
- C++
helpviewer_keywords:
- debugger, DLL crashes
- Module List dialog box
- errors [debugger], DLL crashes
- Modules window
- debugging [Visual Studio], DLL crashes
- DLLs, load order of
ms.assetid: ecf62568-8b65-4a41-b8a4-e962ff2dfb71
caps.latest.revision: 22
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b7af6940de5bd4e39451f44176f5c15d2e8b4548
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2018
ms.locfileid: "51778398"
---
# <a name="how-to-find-which-dll-your-program-crashed-in"></a>方法 : プログラムのクラッシュが発生している DLL を確認する
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

注]
>  実際に画面に表示されるダイアログ ボックスとメニュー コマンドは、アクティブな設定またはエディションによっては、ヘルプの説明と異なる場合があります。 設定を変更するには、[ツール] メニューの [設定のインポートとエクスポート] をクリックします。 詳細については、「 [Visual Studio での開発設定のカスタマイズ](http://msdn.microsoft.com/en-us/22c4debb-4e31-47a8-8f19-16f328d7dcd3)」を参照してください。  
  
 システム DLL または他の開発者が作成したコードを呼び出す部分でアプリケーションがクラッシュした場合、クラッシュが発生した DLL を確認する必要があります。 プログラム外の DLL でクラッシュが発生した場合を使用して場所を識別できます、**モジュール**ウィンドウ。  
  
### <a name="to-find-where-a-crash-occurred-using-the-modules-window"></a>[モジュール] ウィンドウを使ってクラッシュの発生場所を確認するには  
  
1.  クラッシュが発生したアドレスをメモします。  
  
2.  **デバッグ** メニューの 選択**Windows**、 をクリック**モジュール**します。  
  
3.  **モジュール**ウィンドウで、検索、**アドレス**列。 必要に応じて、スクロール バーを使用します。  
  
4.  をクリックして、**アドレス**アドレスによって、Dll を並べ替える列の上部にあるボタンをクリックします。  
  
5.  並べ替えたリストを検索して、アドレス範囲内にクラッシュ場所がある DLL を探します。  
  
6.  見て、**名前**と**パス**DLL の名前とパスを表示する列。  
  
## <a name="see-also"></a>関連項目  
 [方法: ネイティブ Dll のデバッグ](../debugger/how-to-debug-native-dlls.md)   
 [方法 : [モジュール] ウィンドウを使用する](../debugger/how-to-use-the-modules-window.md)





