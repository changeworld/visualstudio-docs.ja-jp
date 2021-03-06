---
title: '方法: XML リテラルに XML スキーマ デザイナーを使用する'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: d11803e7-f81a-41a2-a145-ba494a45cc93
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- VB
ms.workload:
- multiple
ms.openlocfilehash: cc4da90db115e001f7f06ec2e7dd33d64ef20048
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/08/2019
ms.locfileid: "55927283"
---
# <a name="how-to-use-the-xml-schema-designer-with-xml-literals"></a>方法: XML リテラルに XML スキーマ デザイナーを使用します。

このトピックでは、Visual Basic プロジェクトの XML リテラルに関連付けられたスキーマを表示する方法について説明します。

## <a name="to-create-a-new-visual-basic-console-application-project"></a>新しい Visual Basic コンソール アプリケーションのプロジェクトを作成するには

1.  Visual Studio を起動します。

2.  **ファイル**メニューの **新規**、し、**プロジェクト**します。 **[新しいプロジェクト]** ダイアログ ボックスが表示されます。 **プロジェクトの種類**を選択します**他の言語、** 選び**Visual Basic**します。 **テンプレート**、コンソール アプリケーションを選択します。 入力`XMLLiterals`で、**名前**フィールドとプロジェクトの場所、**場所**フィールド。 **[OK]** をクリックします。

     新しいプロジェクトが作成されます。 XMLLiterals プロジェクトには、1 つの Visual Basic ソース ファイルが含まれています。 *Module1.vb*します。

## <a name="to-add-an-existing-xsd-file-to-the-project"></a>既存の XSD ファイルをプロジェクトに追加するには

1.  メモ帳で新しいテキスト ファイルを開きます。 XML スキーマのサンプル コードをコピー[購買発注書のスキーマ](../xml-tools/sample-xsd-file-simple-schema.md)ファイルに貼り付けます。

2.  いくつかの場所に名前でファイルを保存*PurchaseOrderSchema.xsd*します。

3.  **ソリューション エクスプ ローラー**、プロジェクトの名前を右クリックし、選択**追加**、し、**既存項目の**します。 **既存項目の追加** ダイアログ ボックスが表示されます。 参照、 *PurchaseOrderSchema.xsd*ファイル、それを選択してクリックして**追加**します。

     XMLLiterals プロジェクトには、2 つのファイルが含まれています。*Module1.vb*と*PurchaseOrderSchema.xsd*します。

## <a name="to-add-visual-basic-code-with-an-xml-literal-based-on-the-xsd-file-included-in-the-project"></a>プロジェクトに含まれる XSD ファイルに基づいて XML リテラルの Visual Basic コードを追加するには

1. コードに置き換えます*Module1.vb*を次のコード ファイル。

   ```vb
   Imports <xmlns:ns="http://tempuri.org/PurchaseOrderSchema.xsd">

   Module Module1
      Sub Main()

          Dim XMLLiteral = <ns:PurchaseOrder OrderDate="1900-01-01">
                               <ns:ShipTo country="US">
                                   <ns:name>name1</ns:name>
                                   <ns:street>street1</ns:street>
                                   <ns:city>city1</ns:city>
                                   <ns:state>state1</ns:state>
                                   <ns:zip>1</ns:zip>
                               </ns:ShipTo>
                               <ns:BillTo country="US">
                                   <ns:name>name1</ns:name>
                                   <ns:street>street1</ns:street>
                                   <ns:city>city1</ns:city>
                                   <ns:state>state1</ns:state>
                                   <ns:zip>1</ns:zip>
                               </ns:BillTo>
                           </ns:PurchaseOrder>

      End Sub
   End Module
   ```

2. XML リテラルまたは XML 名前空間インポートでの任意の XML ノードを右クリックして**スキーマ エクスプ ローラーで表示する**します。

    **XML スキーマ エクスプ ローラー**が XML スキーマのセットに関連付けられた XML リテラルのある Visual Basic ファイルと並んで表示されます。