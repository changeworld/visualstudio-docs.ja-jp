---
title: WriteContextTLogs | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
apiname:
- WriteContextTLogs
apilocation:
- filetracker.dll
apitype: COM
helpviewer_keywords:
- WriteContextTLogs
ms.assetid: ffc6c7be-3f22-4624-9ffc-0122fe72b6ec
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 722d8c42786a7aaa2daae293b96f7926abcc90ca
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56719835"
---
# <a name="writecontexttlogs"></a>WriteContextTLogs
現在のコンテキストのログ ファイルを書き込みます。

## <a name="syntax"></a>構文

```cpp
HRESULT WINAPI WriteContextTLogs(LPCTSTR intermediateDirectory, LPCTSTR tlogRootName);
```

#### <a name="parameters"></a>パラメーター
[入力] `intermediateDirectory`

 追跡ログを格納するディレクトリ。

[入力] `tlogRootName`

 ログ ファイル名のルート名。

## <a name="return-value"></a>戻り値
 追跡コンテキストが作成された場合、**HRESULT** に **SUCCEEDED** ビットが設定されます。

## <a name="requirements"></a>要件
 **ヘッダー:***FileTracker.h*

## <a name="see-also"></a>関連項目
- [WriteAllTLogs](../msbuild/writealltlogs.md)