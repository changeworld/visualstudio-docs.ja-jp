---
title: SDKReference 要素 (Visual Studio テンプレート) |Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
ms.assetid: 72c8b352-0b7a-42b3-ba5d-2a2d1e90c34b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 692b8600d1de2cbbb17841dd174c4a18010c41d6
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56691164"
---
# <a name="sdkreference-element-visual-studio-templates"></a>SDKReference 要素 (Visual Studio テンプレート)
項目テンプレートが SDK 参照を使用することを指定します。

## <a name="syntax"></a>構文

```xml
<VSTemplate>
    <TemplateContent>
        <References>
            <Reference>
                <SDKReference>SDKname</SDKReference>
```

## <a name="attributes-and-elements"></a>属性および要素
 以降のセクションでは、属性、子要素、および親要素について説明します。

### <a name="attributes"></a>属性
 なし。

### <a name="child-elements"></a>子要素
 なし。

### <a name="parent-elements"></a>親要素

|要素|説明|
|-------------|-----------------|
|[参照](../extensibility/reference-element-visual-studio-templates.md)|項目がプロジェクトに追加されたときに追加するアセンブリ参照を指定します。|

## <a name="text-value"></a>テキスト値
 テキスト値が必要です。

## <a name="remarks"></a>Remarks
 このテキストは、項目テンプレートがインスタンス化されたときに、プロジェクトに追加する SDK 参照を指定します。

```xml
<VSTemplate Version="3.0.0" xmlns="http://schemas.microsoft.com/developer/vstemplate/2005" Type="Item">
    <TemplateData> . . . </TemplateData>
    <TemplateContent>
        <References>
            <Reference>
                <SDKReference>Microsoft Visual C++ Runtime Package, Version=11.0.0.0</SDKReference>
...
```

## <a name="see-also"></a>関連項目
- [References 要素 (Visual Studio テンプレート)](../extensibility/references-element-visual-studio-templates.md)
- [Reference 要素 (Visual Studio テンプレート)](../extensibility/reference-element-visual-studio-templates.md)
- [プロジェクトと項目テンプレートの作成](../ide/creating-project-and-item-templates.md)
- [Visual Studio テンプレート スキーマ参照](../extensibility/visual-studio-template-schema-reference.md)