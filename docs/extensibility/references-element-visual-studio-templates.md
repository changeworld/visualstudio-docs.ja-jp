---
title: 要素 (Visual Studio テンプレート) を参照 |Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#References
helpviewer_keywords:
- <References> element [Visual Studio Templates]
- References element [Visual Studio Templates]
ms.assetid: 1969146d-46bf-422d-8d46-0e9493925003
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3ae0ee308af1502a7c07766e790b79e51f692a96
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56691060"
---
# <a name="references-element-visual-studio-templates"></a>References 要素 (Visual Studio テンプレート)
このテンプレートはプロジェクトに追加するアセンブリ参照をグループ化します。

 \<VSTemplate> \<TemplateContent> \<References>

## <a name="syntax"></a>構文

```xml
<References>
    <Reference>... </Reference>
    <Reference>... </Reference>
    ...
</References>
```

## <a name="attributes-and-elements"></a>属性と要素
 以降のセクションでは、属性、子要素、および親要素について説明します。

### <a name="attributes"></a>属性
 なし。

### <a name="child-elements"></a>子要素

|要素|説明|
|-------------|-----------------|
|[参照](../extensibility/reference-element-visual-studio-templates.md)|必須の要素です。<br /><br /> 項目がプロジェクトに追加されたときに追加するアセンブリ参照を指定します。 1 つまたは複数がある必要があります`Reference`内の要素を`References`要素。|

### <a name="parent-elements"></a>親要素

|要素|説明|
|-------------|-----------------|
|[TemplateContent](../extensibility/templatecontent-element-visual-studio-templates.md)|テンプレートの内容を指定します。|

## <a name="remarks"></a>Remarks
 `References` は、`TemplateContent` の子要素で、省略可能な要素です。

 `Reference`と`References`要素でのみ使用できます *.vstemplate*を持つファイルを`Type`属性の値`Item`します。

## <a name="example"></a>例
 次の例を示しています、`TemplateContent`項目テンプレートの要素。 この XML への参照の追加、 *System.dll*と*System.Data.dll*アセンブリ。

```xml
<TemplateContent>
    <References>
        <Reference>
            <Assembly>
                System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089
            </Assembly>
        </Reference>
        <Reference>
            <Assembly>
                System.Data, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089
            </Assembly>
        </Reference>
    </References>
    ...
</TemplateContent>
```

## <a name="see-also"></a>関連項目
- [Visual Studio テンプレート スキーマ参照](../extensibility/visual-studio-template-schema-reference.md)
- [プロジェクトと項目テンプレートの作成](../ide/creating-project-and-item-templates.md)
