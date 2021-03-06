---
title: marker_importance 列挙型 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- cvmarkersobj/Concurrency::diagnostic::marker_importance
helpviewer_keywords:
- Concurrency::diagnostic::marker_importance enumeration
ms.assetid: d5524ea0-0227-4d8e-9122-332291042df5
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b3f5cfb583ec4fceb9fb7428b08c00f6ca8e26b6
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56613896"
---
# <a name="markerimportance-enumeration"></a>marker_importance 列挙型
コンカレンシー ビジュアライザー マーカーの重要度レベルを表します。

## <a name="syntax"></a>構文

```cpp
enum marker_importance;
```

## <a name="members"></a>メンバー

### <a name="values"></a>値

|name|説明|
|----------|-----------------|
|`critical_importance`|マーカーの重要度がきわめて高いことを指定します。|
|`high_importance`|マーカーの重要度が高いことを指定します。|
|`low_importance`|マーカーの重要度が低いことを指定します。|
|`normal_importance`|マーカーの重要度が標準であることを指定します。|

## <a name="requirements"></a>要件
 **ヘッダー:** *cvmarkersobj.h*

 **名前空間:** Concurrency::diagnostic

## <a name="see-also"></a>関連項目
- [diagnostic 名前空間](../profiling/diagnostic-namespace.md)