---
title: CustomParameter 要素 (Visual Studio テンプレート) |Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#CustomParameter
helpviewer_keywords:
- CustomParameters element [Visual Studio project templates]
ms.assetid: 743c4489-74ac-403a-bbaa-eed7d785a3ac
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: dc0ac3d936037e9b92567a6fcf20b26c25cb5d3f
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56705938"
---
# <a name="customparameter-element-visual-studio-templates"></a>CustomParameter 要素 (Visual Studio テンプレート)
カスタム パラメーターの名前と、テンプレートからプロジェクトまたは項目を作成するときに使用する値が含まれています。

## <a name="syntax"></a>構文

```
<CustomParameter Name="name" Value="value">
```

## <a name="attributes-and-elements"></a>属性と要素
 以降のセクションでは、属性、子要素、および親要素について説明します。

### <a name="attributes"></a>属性

|属性|説明|
|---------------|-----------------|
|`Name`|必須。 パラメーターの名前。 パラメーターの形式は、$*名前*$。|
|`Value`|必須。 パラメーターの置換値。|

### <a name="child-elements"></a>子要素
 なし。

### <a name="parent-elements"></a>親要素

|要素|説明|
|-------------|-----------------|
|[CustomParameters](../extensibility/customparameters-element-visual-studio-templates.md)|このウィザードは、パラメーター置換時に、テンプレートのウィザードに渡されるカスタム パラメーターをグループ化します。|

## <a name="remarks"></a>Remarks
 テンプレートが含まれる場合`CustomParameter`要素、すべてのインスタンス、`Name`属性に置き換え、`Value`で作成したプロジェクトまたは項目のファイル属性。

## <a name="example"></a>例
 次の例では、テンプレートでいくつかのカスタム パラメーターを使用する方法を示します。 次のカスタム パラメーターのすべてのインスタンスを使用してテンプレートからプロジェクトまたは項目を作成するときに`$color1$`と`$color2$`でテンプレート ファイルが置き換えられる`Red`と`Blue`、それぞれします。

```
<CustomParameters>
    <CustomParameter Name="$color1$" Value="Red"/>
    <CustomParameter Name="$color2$" Value="Blue "/>
</CustomParameters>
```

## <a name="see-also"></a>関連項目
- [CustomParameters 要素 (Visual Studio テンプレート)](../extensibility/customparameters-element-visual-studio-templates.md)
- [テンプレート パラメーター](../ide/template-parameters.md)
- [Visual Studio テンプレート スキーマ参照](../extensibility/visual-studio-template-schema-reference.md)