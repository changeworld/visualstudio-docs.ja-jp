---
title: '方法: プログラムによって Outlook の連絡先へのアクセスします。'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- contacts [Office development in Visual Studio], searching
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: c46df4218a12c0f9a155567aeee0c007d0a19c53
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56598207"
---
# <a name="how-to-programmatically-access-outlook-contacts"></a>方法: プログラムによって Outlook の連絡先へのアクセスします。
  この例では、最後の名前が指定した検索文字列を含むすべての連絡先を検索します。

 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

## <a name="example"></a>例
 [!code-csharp[Trin_OL_AccessContacts#1](../vsto/codesnippet/CSharp/Trin_OL_AccessContacts.trin_ol_accesscontacts/thisaddin.cs#1)]
 [!code-csharp[Trin_OL_AccessContacts#1](../vsto/codesnippet/CSharp/Trin_OL_AccessContacts.trin_ol_accesscontacts/thisaddin.cs#1)]
 [!code-vb[Trin_OL_AccessContacts#1](../vsto/codesnippet/VisualBasic/Trin_OL_AccessContacts/thisaddin.vb#1)]

## <a name="compile-the-code"></a>コードのコンパイル
 この例で必要な要素は次のとおりです。

-   連絡先の姓が文字列を含む"**Na"** (Tzipi Butnaru など) で、**連絡先**フォルダー。

## <a name="see-also"></a>関連項目
- [連絡先項目を操作します。](../vsto/working-with-contact-items.md)
- [方法: プログラムによって Outlook の連絡先にエントリを追加します。](../vsto/how-to-programmatically-add-an-entry-to-outlook-contacts.md)
- [方法: プログラムによって特定の連絡先を検索します。](../vsto/how-to-programmatically-search-for-a-specific-contact.md)
- [方法: プログラムによって連絡先から電子メール アドレスを検索します。](../vsto/how-to-programmatically-search-for-an-e-mail-address-in-contacts.md)
- [方法: プログラムによって Outlook の連絡先を削除します。](../vsto/how-to-programmatically-delete-outlook-contacts.md)
