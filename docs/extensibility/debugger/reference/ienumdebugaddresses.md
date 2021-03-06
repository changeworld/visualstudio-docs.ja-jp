---
title: IEnumDebugAddresses |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugAddresses
helpviewer_keywords:
- IEnumDebugAddresses interface
ms.assetid: 5f6f6751-e6d8-4c5a-8e81-414b6e5d8cc5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ac02ca2f22b95b35cc12a545debf081c4052d520
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56702669"
---
# <a name="ienumdebugaddresses"></a>IEnumDebugAddresses
このインターフェイスを実装するオブジェクトのコレクションを表します、 [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)インターフェイス。

## <a name="syntax"></a>構文

```
IEnumDebugAdresses : IUnknown
```

## <a name="notes-for-implementers"></a>実装についてのメモ
 このインターフェイスを実装するオブジェクトのセットを指定するシンボル プロバイダーによって実装されます、 [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)インターフェイス。 存在するための標準 COM 列挙型ではないことに注意してください、 [GetCount](../../../extensibility/debugger/reference/ienumdebugaddresses-getcount.md)メソッド。

## <a name="notes-for-callers"></a>呼び出し元のノート
 このインターフェイスは、によって返される[GetAddressesFromContext](../../../extensibility/debugger/reference/idebugsymbolprovider-getaddressesfromcontext.md)と[GetAddressesFromPosition](../../../extensibility/debugger/reference/idebugsymbolprovider-getaddressesfromposition.md)します。

## <a name="methods-in-vtable-order"></a>Vtable 順序メソッド
 このインターフェイスは、次のメソッドを実装します。

|メソッド|説明|
|------------|-----------------|
|[次へ](../../../extensibility/debugger/reference/ienumdebugaddresses-next.md)|次のセットを取得します。 [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)列挙体からのオブジェクト。|
|[Skip](../../../extensibility/debugger/reference/ienumdebugaddresses-skip.md)|指定されたエントリ数をスキップします。|
|[Reset](../../../extensibility/debugger/reference/ienumdebugaddresses-reset.md)|最初のエントリを列挙型をリセットします。|
|[Clone](../../../extensibility/debugger/reference/ienumdebugaddresses-clone.md)|現在の列挙体のコピーを取得します。|
|[GetCount](../../../extensibility/debugger/reference/ienumdebugaddresses-getcount.md)|列挙内のエントリの数を取得します。|

## <a name="remarks"></a>Remarks
 このインターフェイスは、式エバリュエーターにできるようにする適切なアドレスを確認するためのデバッグ エンジンで通常使用されます。

## <a name="requirements"></a>必要条件
 ヘッダー: sh.h

 名前空間: Microsoft.VisualStudio.Debugger.Interop

 アセンブリ:Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>関連項目
- [シンボルプロバイダーのインターフェイス](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)
- [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)
- [GetAddressesFromContext](../../../extensibility/debugger/reference/idebugsymbolprovider-getaddressesfromcontext.md)
- [GetAddressesFromPosition](../../../extensibility/debugger/reference/idebugsymbolprovider-getaddressesfromposition.md)