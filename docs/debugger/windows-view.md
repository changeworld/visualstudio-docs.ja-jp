---
title: Windows の表示 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.externaltools.spyplus.windowsview
helpviewer_keywords:
- Windows view
ms.assetid: 154786ce-c803-4bfb-8198-f7962a900363
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fef652cbaa83fde61f098fb8fcef9558473fe19a
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56689552"
---
# <a name="windows-view"></a>ウィンドウ ビュー
最初に開いたとき Spy++ は、Windows ビューには、システム内のすべての windows とコントロールのツリーが表示されます。 ウィンドウ ハンドルとクラス名が表示されます。 現在のデスクトップ ウィンドウでは、ツリーの最上部にします。 その他のすべての windows は、デスクトップの子であるし、標準的なウィンドウの階層構造に従って一覧表示されます。 展開できる一覧がその親の下にインデントに兄弟ウィンドウが表示されます。

 次の図は、最上位ノードを展開で一般的な Windows spy++ ビューを示します。

 ![Spy&#43; &#43; Windows ビュー](../debugger/media/spy--_windowsview.png "スパイ + _WindowsView") spy++ Windows ビュー

 現在のデスクトップ ウィンドウでは、ツリーの最上部にします。 その他のすべての windows は、デスクトップの子であるし、は、標準ウィンドウの階層に応じて兄弟ウィンドウが Z オーダーの順に一覧表示します。 展開したり、クリックして、ツリーの任意の親ノードを折りたたむ、+ または - 記号、ノードの横にあります。

 Windows ビューにフォーカスがある場合のファインダー ツールを使用することができます、[ウィンドウ検索 ダイアログ ボックス](../debugger/window-search-dialog-box.md)システムに、ウィンドウを開いてから情報を表示します。

## <a name="in-this-section"></a>このセクションの内容
 [方法: ファインダー ツールを使用して、](../debugger/how-to-use-the-finder-tool.md)このツールがウィンドウのプロパティまたはメッセージをスキャンする方法を示しています。

 [方法: Windows ビューでウィンドウの検索](../debugger/how-to-search-for-a-window-in-windows-view.md)Windows ビューで特定のウィンドウを検索する方法について説明します。

 [方法: ウィンドウの表示プロパティ](../debugger/how-to-display-window-properties.md)ウィンドウ プロパティ ダイアログ ボックスを開くために m プロシージャ。

## <a name="related-sections"></a>関連項目
 [Spy++ ビュー](../debugger/spy-increment-views.md) spy++ ツリー ビュー ウィンドウやメッセージ、プロセス、スレッドのについて説明します。

 [Spy++ の使用](../debugger/using-spy-increment.md)の spy++ ツールを紹介し、使用する方法について説明します。

 [検索ウィンドウ ダイアログ ボックス](../debugger/find-window-dialog-box.md)プロパティまたは特定のウィンドウからメッセージを表示するために使用します。

 [ウィンドウ検索 ダイアログ ボックス](../debugger/window-search-dialog-box.md)Windows ビューで特定のウィンドウのノードを検索するために使用します。

 [ウィンドウのプロパティ ダイアログ ボックス](../debugger/window-properties-dialog-box.md)Windows ビューで選択したウィンドウのプロパティを表示するために使用します。

 [Spy++ リファレンス](../debugger/spy-increment-reference.md)各 spy++ メニューおよびダイアログ ボックスについて説明するセクションが含まれています。