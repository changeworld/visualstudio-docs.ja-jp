﻿---
title: Idiasymbol::get_thunkordinal |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_thunkOrdinal method
ms.assetid: 4b28d78a-1974-4d8a-8bb7-781bf630f2f4
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 78ce8311e9504261399f22feefebb93fb9b3c64f
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56605953"
---
# <a name="idiasymbolgetthunkordinal"></a>IDiaSymbol::get_thunkOrdinal
関数のサンクの型を取得します。

## <a name="syntax"></a>構文

```C++
HRESULT get_thunkOrdinal ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>パラメーター
 `pRetVal`

[out]値を返します、 [THUNK_ORDINAL 列挙型](../../debugger/debug-interface-access/thunk-ordinal.md)関数のサンクの型を指定する列挙体。

## <a name="return-value"></a>戻り値
 成功した場合、返します`S_OK`。 それ以外を返します`S_FALSE`またはエラー コード。

> [!NOTE]
>  戻り値`S_FALSE`プロパティが、シンボルの使用可能なことを意味します。

## <a name="remarks"></a>解説
 このプロパティは有効な場合にのみとしてシンボルを[SymTagEnum 列挙型](../../debugger/debug-interface-access/symtagenum.md)の値`SymTagThunk`します。

 「サンク」は、32 ビット メモリ アドレス空間 (フラットのアドレス空間とも呼ばれます) と (セグメント化されたアドレス空間と呼ばれます)、16 ビットのアドレス空間を変換するコードです。

## <a name="see-also"></a>関連項目
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
- [THUNK_ORDINAL 列挙型](../../debugger/debug-interface-access/thunk-ordinal.md)
- [SymTagEnum 列挙型](../../debugger/debug-interface-access/symtagenum.md)
