---
title: Menus 要素 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSCT XML schema elements, Menus
- Menus element (VSCT XML schema)
ms.assetid: d825a99b-e05c-4dd9-8933-a180216d667a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 96628f3b7050a4ce6f14185033e3d59af63a9de5
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56705600"
---
# <a name="menus-element"></a>Menus 要素
すべてのメニューとツールバー、VSPackage の実装を定義します。

## <a name="syntax"></a>構文

```xml
<Menus>
  <Menu>... </Menu>
  <Menu>... </Menu>
</Menus>
```

## <a name="attributes-and-elements"></a>属性と要素
 以降のセクションでは、属性、子要素、および親要素について説明します。

### <a name="attributes"></a>属性

|属性|説明|
|---------------|-----------------|
|条件|任意。 参照してください[条件付き属性](../extensibility/vsct-xml-schema-conditional-attributes.md)します。|

### <a name="child-elements"></a>子要素

|要素|説明|
|-------------|-----------------|
|[Menus 要素](../extensibility/menus-element.md)|すべてのメニューとツールバー、VSPackage の実装を定義します。|
|[Menu 要素](../extensibility/menu-element.md)|1 つのメニューまたはツールバーを表します。|

### <a name="parent-elements"></a>親要素

|要素|説明|
|-------------|-----------------|
|[Commands 要素](../extensibility/commands-element.md)|VSPackage でのコマンドのコレクションを表します。|

## <a name="example"></a>例

```xml
<Commands package="guidMyPackage">
    <Menus>
      <Menu Condition="'%(DEBUG)' != 'true'"
        guid="cmdSetGuidMyProductCommands" id="menuIDMainMenu"
        priority="0x0000" type="Menu">
        <Annotation>
          <Documentation>this is an annotation</Documentation>
          <AppInfo>
            <CustomData>
              <CustomSubElement>Some data</CustomSubElement>
            </CustomData>
          </AppInfo>
        </Annotation>
        <CommandFlag>AlwaysCreate</CommandFlag>
        <Strings>
          <ButtonText>MainMenu</ButtonText>
        </Strings>
      </Menu>
  </Menus>
<Commands>
```

## <a name="see-also"></a>関連項目
- [Vspackage がユーザー インターフェイス要素を追加する方法](../extensibility/internals/how-vspackages-add-user-interface-elements.md)
- [コマンド、メニューのおよびツールバー](../extensibility/internals/commands-menus-and-toolbars.md)