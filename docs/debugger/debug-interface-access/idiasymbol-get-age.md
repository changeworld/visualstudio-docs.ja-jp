---
title: Idiasymbol::get_age |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_age method
ms.assetid: 60d05654-e832-4a2e-a4a7-fe9922c459fe
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 664b7b5a002e2d30856d072ce77047db6adf7f73
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56624075"
---
# <a name="idiasymbolgetage"></a>IDiaSymbol::get_age
.Pdb ファイルの経過時間の値を取得します。

## <a name="syntax"></a>構文

```C++
HRESULT get_age ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>パラメーター
 `pRetVal`

[out].Pdb ファイルの経過時間の値を返します。

## <a name="return-value"></a>戻り値
 成功した場合、返します`S_OK`。 それ以外を返します`S_FALSE`またはエラー コード。

> [!NOTE]
>  戻り値`S_FALSE`プロパティが、シンボルの使用可能なことを意味します。

## <a name="remarks"></a>解説
 経過時間がある既知の時刻の値に必ずしも対応していませんこれは通常、.pdb ファイルが対応する .exe ファイルと同期していない場合を決定に使用します。

## <a name="requirements"></a>要件

|必要条件|説明|
|-----------------|-----------------|
|ヘッダー:|dia2.h|
|バージョン:|DIA SDK v7.0|

## <a name="see-also"></a>関連項目
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)