---
title: Idiaframedata::get_lengthprolog |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaFrameData::get_lengthProlog method
ms.assetid: 5f042ff1-e74e-430a-be34-d2cf1b18eff2
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ad162a8a29bd9432424ce64d00e820a0bfde1dd9
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56598844"
---
# <a name="idiaframedatagetlengthprolog"></a>IDiaFrameData::get_lengthProlog
プロローグ コード ブロック内のバイト数を取得します。

## <a name="syntax"></a>構文

```C++
HRESULT get_lengthProlog ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>パラメーター
 `pRetVal`

[out]プロローグ コードのバイト数を返します。

## <a name="return-value"></a>戻り値
 正常に終了した場合は、`S_OK` を返します。 返します`S_FALSE`場合、このプロパティはサポートされていません。 それ以外の場合はエラー コードを返します。

## <a name="remarks"></a>解説
 プロローグ コードは、レジスタの保持し、CPU の状態を設定し、関数のスタックを確立する命令のシーケンスです。

## <a name="see-also"></a>関連項目
- [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)