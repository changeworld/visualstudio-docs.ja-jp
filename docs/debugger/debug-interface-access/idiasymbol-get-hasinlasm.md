﻿---
title: Idiasymbol::get_hasinlasm |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_hasInlAsm method
ms.assetid: 7001c7cc-1459-4929-851b-a08066a803c6
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a62126b7e752c8d09a32891e8886be0df07b8d12
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56606336"
---
# <a name="idiasymbolgethasinlasm"></a>IDiaSymbol::get_hasInlAsm
関数がインライン アセンブリを含むかどうかを指定するフラグを取得します。

## <a name="syntax"></a>構文

```C++
HRESULT get_hasInlAsm(
   BOOL *pFlag
);
```

#### <a name="parameters"></a>パラメーター
 `pFlag`

[out]返します`TRUE`場合は、関数は、インライン アセンブリを返しますそれ以外の場合、`FALSE`します。

## <a name="return-value"></a>戻り値
 成功した場合、返します`S_OK`。 それ以外を返します`S_FALSE`またはエラー コード。

> [!NOTE]
>  戻り値`S_FALSE`プロパティがシンボルを使用できないことを意味します。

## <a name="requirements"></a>要件

|必要条件|説明|
|-----------------|-----------------|
|ヘッダー:|dia2.h|
|バージョン:|DIA SDK バージョン 8.0|

## <a name="see-also"></a>関連項目
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
