---
title: スタック フレーム |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- stack frames, debugging
- debugging [Debugging SDK], stack frames
- stack frames
ms.assetid: b5e439d4-1e9d-4e13-9cad-bb8b136d4ca8
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: ebd9f1881f0e0579a3b319f6608cdbf348ed027b
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2018
ms.locfileid: "51789331"
---
# <a name="stack-frames"></a>スタック フレーム
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

デバッガーのアーキテクチャの観点から、**スタック フレーム**:  
  
-   スレッドの実行コンテキストを提供するスタックの抽象化です。 スレッドは、関数内で常に実行されます。 スタック フレームをローカル変数、関数の引数を保持します。 を Visual Studio でデバッグするために、言語またはデバッグ中の環境は、スタック フレームをサポートする必要があります。  
  
-   両方を特定し、それ自体を記述および関連付けられたスレッドを返すことができます。 スタック フレームを返すことも、現在の命令ポインターだけでなく、関連付けられているドキュメントを表す、コードのコンテキストや式の評価コンテキスト。  
  
-   名前、種類、およびローカル変数と引数の値を記述して、さまざまな IDE のデバッグ ウィンドウに表示されるプロパティがあります。  
  
-   によって表される、 [IDebugStackFrame2](../../extensibility/debugger/reference/idebugstackframe2.md)デバッグ エンジン (DE) またはスレッドの実行の結果として、仮想マシンによって作成された通常のインターフェイス。  
  
## <a name="see-also"></a>関連項目  
 [デバッガー コンテキスト](../../extensibility/debugger/debugger-contexts.md)   
 [デバッガーの概念](../../extensibility/debugger/debugger-concepts.md)   
 [デバッグ エンジン](../../extensibility/debugger/debug-engine.md)   
 [IDebugStackFrame2](../../extensibility/debugger/reference/idebugstackframe2.md)

