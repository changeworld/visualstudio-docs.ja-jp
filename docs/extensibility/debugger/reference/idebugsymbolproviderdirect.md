---
title: IDebugSymbolProviderDirect |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugSymbolProviderDirect interface
ms.assetid: 872b04a8-70de-4ab5-aceb-684c81828545
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d546cae810d40a850bb3dd2758f2f659eecdd18e
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56697429"
---
# <a name="idebugsymbolproviderdirect"></a>IDebugSymbolProviderDirect
メタデータとコアのシンボル インターフェイスに直接アクセスするシンボル プロバイダーを表します。

## <a name="syntax"></a>構文

```
IDebugSymbolProviderDirect: IUnknown
```

## <a name="methods"></a>メソッド
 このインターフェイスは、次のメソッドを実装します。

|メソッド|説明|
|------------|-----------------|
|[GetAppIDFromAddress](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getappidfromaddress.md)|デバッグ アドレスが指定されて、アプリケーション ドメインの識別子を取得します。|
|[GetCurrentModulesInfo](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getcurrentmodulesinfo.md)|シンボルのグループ内のモジュールに関する情報を取得します。|
|[GetCurrentModulesState](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getcurrentmodulesstate.md)|シンボル プロバイダーがメンバーであるシンボルのグループに関する情報を取得します。|
|[GetMetaDataImport](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getmetadataimport.md)|メタデータ情報のインポートを取得します。|
|[GetMethodFromAddress](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getmethodfromaddress.md)|指定されたデバッグ アドレスには、方法に関する情報を取得します。|
|[GetSymUnmanagedReader](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getsymunmanagedreader.md)|アンマネージ コードのシンボル リーダーを取得します。|

## <a name="remarks"></a>Remarks
 このインターフェイスは、その他のシンボル プロバイダー インターフェイスのほとんどではなく使用できます。 メタデータへの直接アクセスを提供し、`CorSym`インターフェイス。

## <a name="requirements"></a>必要条件
 ヘッダー:Sh.h

 名前空間: Microsoft.VisualStudio.Debugger.Interop

 アセンブリ:Microsoft.VisualStudio.Debugger.Interop.dll