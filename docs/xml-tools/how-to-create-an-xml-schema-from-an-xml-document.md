---
title: '方法: XML ドキュメントから XML スキーマを作成する'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 1d6700a9-fd67-4794-8997-399589e99bec
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ebea3b20bc606ec82529e4a9b2a547d6a44fc905
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/08/2019
ms.locfileid: "55953790"
---
# <a name="how-to-create-an-xml-schema-from-an-xml-document"></a>方法: XML ドキュメントから XML スキーマを作成します。

XML エディターを使用することで、XML ドキュメントから XML スキーマ定義言語 (XSD) スキーマを作成することができます。 スキーマがどのように生成されるかは、XML インスタンス ドキュメントによって、次の方法で決定されます。

-   XML ドキュメントにスキーマまたはドキュメント型定義 (DTD) が関連付けられていない場合は、新しい XML スキーマを推論するために XML ドキュメント内のデータが使用されます。

-   関連する DTD が XML ドキュメントに含まれている場合は、外部 DTD および内部サブセットが、対応する XML スキーマに変換されます。

-   インラインの XDR (XML-Data Reduced) スキーマが XML ドキュメントに含まれている場合は、その XDR スキーマが、対応する XML スキーマに変換されます。

作成されたスキーマは次に、XML ドキュメントで IntelliSense を利用できるようにするために使用されます。

スキーマ推論エンジンの詳細については、次を参照してください。 [XML スキーマの推論](/dotnet/standard/data/xml/inferring-an-xml-schema)します。

## <a name="to-create-an-xml-schema"></a>XML スキーマを作成するには

1.  XML インスタンス ドキュメントを XML エディターに読み込みます。

2.  をクリックして、 **Create Schema**からボタン、**ツールバー**します。

     XML インスタンス ドキュメントで見つかった名前空間ごとに 1 つの XML スキーマ ドキュメントが作成され、開かれます。 各スキーマは、一時的にその他のファイルとして開かれます。

     スキーマは、ディスクに保存するか、プロジェクトに追加するか、破棄することができます。

    > [!NOTE]
    >  **Create Schema**コマンドは、XML エディターのとでは、ショートカット メニューからも、 **XML**メニュー。

## <a name="see-also"></a>関連項目

- [XML エディター](../xml-tools/xml-editor.md)