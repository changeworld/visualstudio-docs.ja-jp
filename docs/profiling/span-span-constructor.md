---
title: span::span コンストラクター | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- cvmarkersobj/Concurrency::diagnostic::span::span
helpviewer_keywords:
- Concurrency::diagnostic::span constructor
ms.assetid: 8b5578aa-5e5c-4ac7-87c7-ce87c4246e2c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3b04f9edc946b83f8785c6a6fb3e9720db4840f0
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56596199"
---
# <a name="spanspan-constructor"></a>span::span コンストラクター
`span` クラスの新しいインスタンスを初期化します。

## <a name="syntax"></a>構文

```cpp
span(
   const marker_series& _Series,
   _In_ LPCTSTR _Format,
   ...
);
span(
   const marker_series& _Series,
   marker_importance _Importance,
   _In_ LPCTSTR _Format,
   ...
);
span(
   const marker_series& _Series,
   int _Category,
   _In_ LPCTSTR _Format,
   ...
);
span(
   const marker_series& _Series,
   marker_importance _Importance,
   int _Category,
   _In_ LPCTSTR _Format,
   ...
);
```

#### <a name="parameters"></a>パラメーター
 `_Series` 有効なマーカー シリーズ コンテキスト。

 `_Format` 0 個以上の書式項目が混在したテキストを含む複合書式指定文字列。各書式項目は、引数リスト内のオブジェクトに対応します。

 `_Importance` 重要度レベル。

 `_Category` カテゴリ。

## <a name="requirements"></a>要件
 **ヘッダー:** *cvmarkersobj.h*

 **名前空間:** Concurrency::diagnostic

 ## <a name="see-also"></a>関連項目
- [span クラス](../profiling/span-class.md)