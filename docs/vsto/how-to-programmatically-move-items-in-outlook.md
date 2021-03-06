---
title: '方法: プログラムによって Outlook でアイテムを移動します。'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Outlook folders [Office development in Visual Studio], moving items
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 10b0f05e758f71830d5377c738ff9dee683022b8
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56641625"
---
# <a name="how-to-programmatically-move-items-in-outlook"></a>方法: プログラムによって Outlook でアイテムを移動します。
  この例から未読の電子メール メッセージの移動、**受信トレイ**という名前のフォルダーに**テスト**します。 例では、のみ、単語が含まれているメッセージを移動**テスト**で、`Subject`フィールド。

 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

## <a name="example"></a>例
 [!code-csharp[Trin_OL_MoveItems#1](../vsto/codesnippet/CSharp/Trin_OL_MoveItems/thisaddin.cs#1)]

## <a name="compile-the-code"></a>コードのコンパイル
 この例で必要な要素は次のとおりです。

-   という名前の Outlook メール フォルダー**テスト**します。

-   電子メール メッセージが到着する単語**テスト**で、`Subject`フィールド。

## <a name="see-also"></a>関連項目
- [フォルダーを操作します。](../vsto/working-with-folders.md)
- [方法: 名前でフォルダーをプログラムで取得します。](../vsto/how-to-programmatically-retrieve-a-folder-by-name.md)
- [方法: プログラムによって特定のフォルダー内を検索します。](../vsto/how-to-programmatically-search-within-a-specific-folder.md)
- [方法: プログラムで電子メール メッセージを受信したときにアクションを実行します。](../vsto/how-to-programmatically-perform-actions-when-an-e-mail-message-is-received.md)
