﻿---
title: Idiasymbol::get_hasseh |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_hasSEH method
ms.assetid: 1a709ded-22c8-464c-97be-eba5e464210c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6bf5d6f31d25d72cd6bc71f9d8b17443b3d8fc8a
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56643731"
---
# <a name="idiasymbolgethasseh"></a>IDiaSymbol::get_hasSEH
関数がいずれかを含めるかどうかを指定するフラグを取得します。[構造化例外処理 (c/c++)](/cpp/cpp/structured-exception-handling-c-cpp) (例: _ _try/\__except ブロック)。

## <a name="syntax"></a>構文

```C++
HRESULT get_hasSEH(
   BOOL *pFlag
);
```

#### <a name="parameters"></a>パラメーター
 `pFlag`

[out]返します`TRUE`メンバー関数に構造化例外処理ブロックがある場合は、関数を返しますそれ以外の場合、`FALSE`します。

## <a name="return-value"></a>戻り値
 成功した場合、返します`S_OK`。 それ以外を返します`S_FALSE`またはエラー コード。

> [!NOTE]
>  戻り値`S_FALSE`プロパティが、シンボルの使用可能なことを意味します。

## <a name="requirements"></a>要件

|必要条件|説明|
|-----------------|-----------------|
|ヘッダー:|dia2.h|
|バージョン:|DIA SDK バージョン 8.0|

## <a name="see-also"></a>関連項目
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
- [構造化例外処理 (C/C++)](/cpp/cpp/structured-exception-handling-c-cpp)
