---
title: Groups 要素 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSCT XML schema elements, Groups
- Groups element (VSCT XML schema)
ms.assetid: 740ca4ec-79fa-4b98-8f9a-2a137f9f7f98
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 197c2890613ac376b8c494467b86576b1980b00b
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56723228"
---
# <a name="groups-element"></a>Groups 要素
VSPackage のコマンド グループを定義するエントリが含まれています。

## <a name="syntax"></a>構文

```xml
<Groups>
  <Group>... </Group>
  <Group>... </Group>
</Groups>
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
|[Group 要素](../extensibility/group-element.md)|1 つのコマンド グループを表します。|
|[Groups 要素](../extensibility/groups-element.md)|VSPackage のコマンド グループを定義するエントリが含まれています。|

### <a name="parent-elements"></a>親要素

|要素|説明|
|-------------|-----------------|
|[Commands 要素](../extensibility/commands-element.md)|VSPackage のツールバーのコマンドのコレクションを表します。|

## <a name="example"></a>例

```xml
<Groups>
  <Group guid="cmdSetGuidWidgetCommands" id="groupIDFileEdit">
    <Parent guid="guidSHLMainMenu" id="IDM_VS_TOOL_MAINMENU"/>
  </Group>
</Groups>
```

## <a name="see-also"></a>関連項目
- [Vspackage がユーザー インターフェイス要素を追加する方法](../extensibility/internals/how-vspackages-add-user-interface-elements.md)
- [コマンド、メニューのおよびツールバー](../extensibility/internals/commands-menus-and-toolbars.md)