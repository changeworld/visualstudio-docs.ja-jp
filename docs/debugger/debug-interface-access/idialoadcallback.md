---
title: IDiaLoadCallback |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaLoadCallback interface
ms.assetid: 2f18c64c-2cf0-43fc-a447-21e82702ca2a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 353e7dcbe1bcc44b9e8b7e9c7c417913ef07be35
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56618875"
---
# <a name="idialoadcallback"></a>IDiaLoadCallback
プロシージャの検索、したがって、ユーザー インターフェイスの場所の試行の進行状況の報告を有効にする DIA シンボルからのコールバックを受け取ります。

## <a name="syntax"></a>構文

```
IDiaLoadCallback : IUnknown
```

## <a name="methods-in-vtable-order"></a>Vtable 順序のメソッド
 次のメソッドは、このインターフェイスによって公開されます。

|メソッド|説明|
|------------|-----------------|
|[IDiaLoadCallback::NotifyDebugDir](../../debugger/debug-interface-access/idialoadcallback-notifydebugdir.md)|.Exe ファイルでデバッグ ディレクトリが見つかったときに呼び出されます。|
|[IDiaLoadCallback::NotifyOpenDBG](../../debugger/debug-interface-access/idialoadcallback-notifyopendbg.md)|候補 .dbg ファイルが開かれたときに呼び出されます。|
|[IDiaLoadCallback::NotifyOpenPDB](../../debugger/debug-interface-access/idialoadcallback-notifyopenpdb.md)|候補の .pdb ファイルが開かれたときに呼び出されます。|
|[IDiaLoadCallback::RestrictRegistryAccess](../../debugger/debug-interface-access/idialoadcallback-restrictregistryaccess.md)|シンボルの検索パスを検索するレジストリのクエリを使用できるかどうかを決定します。|
|[IDiaLoadCallback::RestrictSymbolServerAccess](../../debugger/debug-interface-access/idialoadcallback-restrictsymbolserveraccess.md)|シンボルを解決するのには、シンボル サーバーへのアクセスが許可されたかどうかを決定します。|

## <a name="remarks"></a>解説
 クライアント アプリケーションは、このインターフェイスを実装しへの呼び出しでの参照を提供します、 [idiadatasource::loaddataforexe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)メソッド。

 読み込みプロセスで適用可能な追加の制限事項を参照してください、 [IDiaLoadCallback2](../../debugger/debug-interface-access/idialoadcallback2.md)インターフェイス。

## <a name="requirements"></a>要件
 ヘッダー: Dia2.h

 ライブラリ: diaguids.lib

 DLL: msdia80.dll

## <a name="see-also"></a>関連項目
- [インターフェイス (Debug Interface Access SDK)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)
- [IDiaDataSource::loadDataForExe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)
- [IDiaReadExeAtOffsetCallback](../../debugger/debug-interface-access/idiareadexeatoffsetcallback.md)
- [IDiaReadExeAtRVACallback](../../debugger/debug-interface-access/idiareadexeatrvacallback.md)
- [IDiaLoadCallback2](../../debugger/debug-interface-access/idialoadcallback2.md)