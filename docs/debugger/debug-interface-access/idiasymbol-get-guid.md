﻿---
title: Idiasymbol::get_guid |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_guid method
ms.assetid: c02a6c92-f406-4646-82e7-3cd005af900e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7c2440fb6d35594825540fb249a8d2d3a9ba683d
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56611088"
---
# <a name="idiasymbolgetguid"></a>IDiaSymbol::get_guid
シンボルのグローバル一意識別子 (GUID) を取得します。

## <a name="syntax"></a>構文

```C++
HRESULT get_guid ( 
   GUID* pRetVal
);
```

#### <a name="parameters"></a>パラメーター
 `pRetVal`

[out]シンボルの GUID を返します。

## <a name="return-value"></a>戻り値
 成功した場合、返します`S_OK`。 それ以外を返します`S_FALSE`またはエラー コード。

> [!NOTE]
>  戻り値`S_FALSE`プロパティが、シンボルの使用可能なことを意味します。

## <a name="requirements"></a>要件

|必要条件|説明|
|-----------------|-----------------|
|ヘッダー:|dia2.h|
|バージョン:|DIA SDK v7.0|

## <a name="see-also"></a>関連項目
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
