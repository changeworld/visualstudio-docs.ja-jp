---
title: SccEndBatch 関数 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccEndBatch
helpviewer_keywords:
- SccEndBatch function
ms.assetid: 100e7833-fe0a-45c0-9fca-3e61fd1165b7
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e0662e4c4d1d71e2c9ae0e8f40ff21868d6b9a5d
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56683923"
---
# <a name="sccendbatch-function"></a>SccEndBatch 関数
この関数は、ソース管理操作のバッチを終了します。 これらのバッチは、入れ子にできません。

## <a name="syntax"></a>構文

```cpp
SCCRTN SccEndBatch(void);
```

## <a name="parameters"></a>パラメーター
 なし。

## <a name="return-value"></a>戻り値
 この関数のソース管理プラグイン実装は、次の値のいずれかを返すが必要です。

|[値]|説明|
|-----------|-----------------|
|SCC_OK|操作のバッチを正常に終了しました。|
|SCC_E_UNKNOWNERROR|不特定のエラーです。|

## <a name="remarks"></a>Remarks
 ソース コントロールのバッチを使用して、複数のプロジェクトまたは複数のコンテキスト全体で同じソース管理操作を実行できます。 バッチを使用して、バッチ操作中に、ユーザー エクスペリエンスから冗長ダイアログ ボックスを解消できます。 [SccBeginBatch](../extensibility/sccbeginbatch-function.md)と`SccEndBatch`を先頭と末尾の操作を示すために、ペアとして関数が使用されます。 入れ子にできません。

## <a name="see-also"></a>関連項目
- [ソース管理プラグイン API 関数](../extensibility/source-control-plug-in-api-functions.md)
- [SccBeginBatch](../extensibility/sccbeginbatch-function.md)