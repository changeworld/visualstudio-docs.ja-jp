---
title: '方法: プログラムによって Word の表を作成します。'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], adding tables
- tables [Office development in Visual Studio], adding to documents
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 10683f2bd740a92b41c0063da15d093248396bd5
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56619395"
---
# <a name="how-to-programmatically-create-word-tables"></a>方法: プログラムによって Word の表を作成します。
  <xref:Microsoft.Office.Interop.Word.Tables> コレクションは <xref:Microsoft.Office.Interop.Word.Document>、<xref:Microsoft.Office.Tools.Word.Document>、<xref:Microsoft.Office.Interop.Word.Selection>、および <xref:Microsoft.Office.Interop.Word.Range> の各クラスのメンバーです。したがって、これらのどのコンテキストでも表を作成できます。 指定した範囲に表を追加するには、<xref:Microsoft.Office.Interop.Word.Tables> コレクションの <xref:Microsoft.Office.Interop.Word.Tables.Add%2A> メソッドを使用します。

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

## <a name="create-tables-in-document-level-customizations"></a>ドキュメント レベルのカスタマイズでテーブルを作成します。

### <a name="to-add-a-table-to-a-document"></a>ドキュメントにテーブルを追加するには

- <xref:Microsoft.Office.Interop.Word.Tables.Add%2A> メソッドを使用して、ドキュメントの先頭に 3 行 4 列の表を追加します。

   次のコード例を使用するには、プロジェクトの `ThisDocument` クラスから実行します。

   [!code-vb[Trin_VstcoreWordAutomation#86](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#86)]
   [!code-csharp[Trin_VstcoreWordAutomation#86](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#86)]

  表を作成すると、作成した表は自動的に <xref:Microsoft.Office.Tools.Word.Document> ホスト項目の <xref:Microsoft.Office.Interop.Word.Tables> コレクションに追加されます。 表を参照するには、次のコードに示すとおり、<xref:Microsoft.Office.Interop.Word.Tables.Item%2A> プロパティを使用して項目番号で参照します。

### <a name="to-refer-to-a-table-by-item-number"></a>項目番号で表を参照するには

1. <xref:Microsoft.Office.Interop.Word.Tables.Item%2A> プロパティを使用して、参照する表の項目番号を指定します。

    次のコード例を使用するには、プロジェクトの `ThisDocument` クラスから実行します。

    [!code-vb[Trin_VstcoreWordAutomation#87](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#87)]
    [!code-csharp[Trin_VstcoreWordAutomation#87](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#87)]

   各 <xref:Microsoft.Office.Interop.Word.Table> オブジェクトには <xref:Microsoft.Office.Interop.Word.Table.Range%2A> プロパティもあり、このプロパティを使用して書式設定属性を設定できます。

### <a name="to-apply-a-style-to-a-table"></a>表にスタイルを適用するには

1.  <xref:Microsoft.Office.Interop.Word.Table.Style%2A> プロパティを使用して、Word のいずれかの組み込みスタイルを表に適用します。

     次のコード例を使用するには、プロジェクトの `ThisDocument` クラスから実行します。

     [!code-vb[Trin_VstcoreWordAutomation#88](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#88)]
     [!code-csharp[Trin_VstcoreWordAutomation#88](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#88)]

## <a name="create-tables-in-vsto-add-ins"></a>VSTO アドインでテーブルを作成します。

### <a name="to-add-a-table-to-a-document"></a>ドキュメントにテーブルを追加するには

- <xref:Microsoft.Office.Interop.Word.Tables.Add%2A> メソッドを使用して、ドキュメントの先頭に 3 行 4 列の表を追加します。

   作業中のドキュメントに表を追加するコード例を次に示します。 このコード例を使用するには、プロジェクトの `ThisAddIn` クラスから実行します。

   [!code-vb[Trin_VstcoreWordAutomationAddIn#86](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#86)]
   [!code-csharp[Trin_VstcoreWordAutomationAddIn#86](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#86)]

  表を作成すると、作成した表は自動的に <xref:Microsoft.Office.Interop.Word.Document> の <xref:Microsoft.Office.Interop.Word.Tables> コレクションに追加されます。 表を参照するには、次のコードに示すとおり、<xref:Microsoft.Office.Interop.Word.Tables.Item%2A> プロパティを使用して項目番号で参照します。

### <a name="to-refer-to-a-table-by-item-number"></a>項目番号で表を参照するには

1. <xref:Microsoft.Office.Interop.Word.Tables.Item%2A> プロパティを使用して、参照する表の項目番号を指定します。

    作業中のドキュメントを使用するコード例を次に示します。 このコード例を使用するには、プロジェクトの `ThisAddIn` クラスから実行します。

    [!code-vb[Trin_VstcoreWordAutomationAddIn#87](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#87)]
    [!code-csharp[Trin_VstcoreWordAutomationAddIn#87](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#87)]

   各 <xref:Microsoft.Office.Interop.Word.Table> オブジェクトには <xref:Microsoft.Office.Interop.Word.Table.Range%2A> プロパティもあり、このプロパティを使用して書式設定属性を設定できます。

### <a name="to-apply-a-style-to-a-table"></a>表にスタイルを適用するには

1.  <xref:Microsoft.Office.Interop.Word.Table.Style%2A> プロパティを使用して、Word のいずれかの組み込みスタイルを表に適用します。

     作業中のドキュメントを使用するコード例を次に示します。 このコード例を使用するには、プロジェクトの `ThisAddIn` クラスから実行します。

     [!code-vb[Trin_VstcoreWordAutomationAddIn#88](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#88)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#88](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#88)]

## <a name="see-also"></a>関連項目
- [方法: プログラムによって Word の表のセルにテキストと書式を追加します。](../vsto/how-to-programmatically-add-text-and-formatting-to-cells-in-word-tables.md)
- [方法: プログラムによって Word の表に行と列を追加します。](../vsto/how-to-programmatically-add-rows-and-columns-to-word-tables.md)
- [方法: プログラムによって document プロパティを Word の表に読み込む](../vsto/how-to-programmatically-populate-word-tables-with-document-properties.md)
- [Office ソリューションの省略可能なパラメーター](../vsto/optional-parameters-in-office-solutions.md)
