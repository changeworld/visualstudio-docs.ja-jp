---
title: '方法: プログラムによって文書からすべてのコメントを削除します。'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], removing comments
- comments, removing from documents
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: fadc8830649a15f1785194f3e2640a7ee86fadbb
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56644589"
---
# <a name="how-to-programmatically-remove-all-comments-from-documents"></a>方法: プログラムによって文書からすべてのコメントを削除します。
  `DeleteAllComments` メソッドを使用して、Microsoft Office Word 文書からすべてのコメントを削除します。

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

## <a name="to-remove-all-comments-from-a-document-that-is-part-of-a-document-level-customization"></a>ドキュメント レベルのカスタマイズの一部であるドキュメントから、すべてのコメントを削除するには

1.  プロジェクトの <xref:Microsoft.Office.Tools.Word.Document.DeleteAllComments%2A> クラスの `ThisDocument` メソッドを呼び出します。 このコード例を使用するには、 `ThisDocument` クラスからコードを実行します。

     [!code-vb[Trin_VstcoreWordAutomation#119](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#119)]
     [!code-csharp[Trin_VstcoreWordAutomation#119](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#119)]

## <a name="to-remove-all-comments-from-a-document-by-using-a-vsto-add-in"></a>VSTO アドインを使用して、ドキュメントからすべてのコメントを削除するには

1.  コメントを削除する <xref:Microsoft.Office.Interop.Word._Document.DeleteAllComments%2A> から <xref:Microsoft.Office.Interop.Word.Document> メソッドを呼び出します。

     次に示すコード例では、アクティブ ドキュメントからすべてのコメントを削除します。 このコード例を使用するには、プロジェクトの `ThisAddIn` クラスからコードを実行します。

     [!code-vb[Trin_VstcoreWordAutomationAddIn#119](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#119)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#119](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#119)]

## <a name="see-also"></a>関連項目
- [方法: プログラムによって文書内のテキストにコメントを追加します。](../vsto/how-to-programmatically-add-comments-to-text-in-documents.md)
- [Document ホスト項目](../vsto/document-host-item.md)
