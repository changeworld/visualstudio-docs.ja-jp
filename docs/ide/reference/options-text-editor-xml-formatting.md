---
title: '[オプション]、[テキスト エディター]、[XML]、[書式設定]'
ms.date: 10/29/2018
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.XML.Formatting
ms.assetid: 203e60b2-7b80-4ff4-9fa1-aa9f4374377b
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 8452410235226b3d7a1446d7a8c5a2ee709eff6e
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/08/2019
ms.locfileid: "55943546"
---
# <a name="options-text-editor-xml-formatting"></a>[オプション]、[テキスト エディター]、[XML]、[書式設定]

**[書式設定]** プロパティ ページでは、XML ドキュメントで要素と属性を書式設定する方法を指定します。 **[オプション]** ダイアログ ボックスを開くには、**[ツール]** メニューをクリックし、**[オプション]** をクリックします。 **[書式設定]** プロパティ ページにアクセスするには、**[テキスト エディター]** > **[XML]** > **[書式設定]** ノードを展開します。

## <a name="attributes"></a>属性

**手動による属性の書式設定を保持する**

属性を再フォーマットしません。 これが既定の設定です。

> [!NOTE]
> 属性が複数行にわたっている場合、エディターは親要素のインデントに対応するように属性の各行にインデントを設定します。

**各行の属性の記述位置を揃える**

最初の属性のインデントに対応するように、2 番目およびそれ以降の行頭を揃えて配置します。 XML テキストで属性がどのように並べられるかについて例を次に示します。

```xml
<item id = "123-A"
      name = "hammer"
      price = "9.95">
</item>
```

## <a name="auto-reformat"></a>自動による書式の再設定

**クリップボードからの貼り付け時**

クリップボードから貼り付ける XML テキストを再フォーマットします。

**終了タグの完成時**

終了タグが完了したときに要素を再フォーマットします。

## <a name="mixed-content"></a>混合コンテンツ

**混合したコンテンツを既定でフォーマットする**

コンテンツが `xml:space="preserve"` スコープで見つかった場合を除き、混合コンテンツの再フォーマットを試みます。 これが既定の設定です。

要素にテキストとマークアップが混在して含まれている場合、そのコンテンツは混合コンテンツと見なされます。 混合コンテンツを持つ要素の例を次に示します。

```xml
<dir>c:\data\AlphaProject\
  <file readOnly="false">test1.txt</file>
  <file readOnly="false">test2.txt</file>
</dir>
```

## <a name="see-also"></a>関連項目

- [方法: XML ドキュメントを作成する (Visual Basic)](/dotnet/visual-basic/programming-guide/program-structure/how-to-create-xml-documentation)
- [コード生成](../code-generation-in-visual-studio.md)