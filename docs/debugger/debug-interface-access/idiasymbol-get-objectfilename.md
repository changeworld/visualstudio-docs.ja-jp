﻿---
title: IDiaSymbol::get_objectFileName |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 21793872-4879-4e4d-b527-dcf70aa7fb31
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 841fe2b1ae6f54b3bc7deea97b335790ca6dac5f
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56611816"
---
# <a name="idiasymbolgetobjectfilename"></a>IDiaSymbol::get_objectFileName
オブジェクト ファイルの名前を取得します。

## <a name="syntax"></a>構文

```C++
HRESULT get_objectFilename(
   BSTR *pRetVal);
```

#### <a name="parameters"></a>パラメーター
 `pRetVal`

[out]ポインターを`BSTR`オブジェクト ファイルの名前を保持しています。

## <a name="return-value"></a>戻り値
 成功した場合、返します`S_OK`。 それ以外を返します`S_FALSE`またはエラー コード。

## <a name="see-also"></a>関連項目
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
