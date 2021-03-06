---
title: IDebugEngine3 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEngine3
helpviewer_keywords:
- IDebugEngine3 interface
ms.assetid: 8bdf4bb7-3b5d-4991-8981-772d4f6bb656
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c043a05d2656dc1cc56377ad061854cd1aca9e7c
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56709539"
---
# <a name="idebugengine3"></a>IDebugEngine3
1 つまたは複数のモジュールのデバッグを制御する 1 つのデバッグ エンジン (DE) を表します。

## <a name="syntax"></a>構文

```
IDebugEngine3 : IDebugEngine2
```

## <a name="notes-for-implementers"></a>実装についてのメモ
 このインターフェイスはカスタム DE (シンボルをサポートする) 場合 JustMyCode 状態を有効にします。 シンボルと JustMyCode をサポートしている場合、DE によってこのインターフェイスを実装する必要があります。

## <a name="notes-for-callers"></a>呼び出し元のノート
 このインターフェイスは、セッション デバッグ マネージャー (SDM) シンボルの読み込み元の場所のオプションをユーザーに渡すによって呼び出されます。 インスタンス化されるときに、エンジンの GUID を設定するためにも呼び出されます (この GUID は、エンジンの登録時からのメトリックに基づく)。 SDM も JustMyCode 状態を設定して、指定された状態にデバッガーによって認識されているすべての例外を設定するのには、このインターフェイスを呼び出します。

## <a name="methods-in-vtable-order"></a>Vtable 順序のメソッド
 継承されたメソッドだけでなく[IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)、`IDebugEngine3`インターフェイスは、次のメソッドを公開します。

|メソッド|説明|
|------------|-----------------|
|[SetSymbolPath](../../../extensibility/debugger/reference/idebugengine3-setsymbolpath.md)|デがデバッグ シンボルの検索に使用するパスまたはパスを設定します。|
|[LoadSymbols](../../../extensibility/debugger/reference/idebugengine3-loadsymbols.md)|シンボルが読み込まれてしていないすべてのモジュールのシンボルを読み込みます。|
|[SetJustMyCodeState](../../../extensibility/debugger/reference/idebugengine3-setjustmycodestate.md)|JustMyCode 情報の詳細、DE に指示します。|
|[SetEngineGuid](../../../extensibility/debugger/reference/idebugengine3-setengineguid.md)|メトリックから DE GUID を設定します。|
|[SetAllExceptions](../../../extensibility/debugger/reference/idebugengine3-setallexceptions.md)|指定された状態に、現在未処理のすべての例外を設定します。|

## <a name="requirements"></a>必要条件
 ヘッダー: msdbg.h

 名前空間: Microsoft.VisualStudio.Debugger.Interop

 アセンブリ:Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>関連項目
- [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)