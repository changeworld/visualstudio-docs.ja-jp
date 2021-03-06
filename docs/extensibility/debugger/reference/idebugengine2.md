---
title: IDebugEngine2 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEngine2
helpviewer_keywords:
- IDebugEngine2 interface
ms.assetid: 1f0e9ac0-6dfb-461a-976c-888d82144cdb
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 86458a501ba1bb321727663b6c8b995d329904f7
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56707576"
---
# <a name="idebugengine2"></a>IDebugEngine2
このインターフェイスは、デバッグ エンジン (DE) を表します。 設定され、例外をオフにするとブレークポイントの作成からデバッグ セッションのさまざまな側面を管理に使用されます。

## <a name="syntax"></a>構文

```
IDebugEngine2 : IUnknown
```

## <a name="notes-for-implementers"></a>実装についてのメモ
 このインターフェイスは、プログラムのデバッグを管理するカスタム DE によって実装されます。 このインターフェイスは、DE で実装する必要があります。

## <a name="notes-for-callers"></a>呼び出し元のノート
 このインターフェイスは、セッション デバッグ マネージャーの例外の管理、ブレークポイントを作成、デにより送信された同期イベントに応答してなど、デバッグ セッションを管理するには、(SDM) によって呼び出されます。

## <a name="methods-in-vtable-order"></a>Vtable 順序のメソッド
 次の表は、メソッドの`IDebugEngine2`します。

|メソッド|説明|
|------------|-----------------|
|[EnumPrograms](../../../extensibility/debugger/reference/idebugengine2-enumprograms.md)|ドイツでは、デバッグされているすべてのプログラムの列挙子を作成します。|
|[Attach](../../../extensibility/debugger/reference/idebugengine2-attach.md)|プログラムを DE にアタッチします。|
|[CreatePendingBreakpoint](../../../extensibility/debugger/reference/idebugengine2-creatependingbreakpoint.md)|デに保留中のブレークポイントを作成します。|
|[SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md)|デが特定の例外を処理する方法を指定します。|
|[RemoveSetException](../../../extensibility/debugger/reference/idebugengine2-removesetexception.md)|不要になったデバッグ エンジンによって処理されるように指定された例外を削除します。|
|[RemoveAllSetExceptions](../../../extensibility/debugger/reference/idebugengine2-removeallsetexceptions.md)|例外は、IDE が特定のランタイム アーキテクチャまたは言語の設定の一覧を削除します。|
|[GetEngineID](../../../extensibility/debugger/reference/idebugengine2-getengineid.md)|デの GUID を取得します。|
|[DestroyProgram](../../../extensibility/debugger/reference/idebugengine2-destroyprogram.md)|指定されたプログラムが正しく終了になっていると、DE がプログラムへのすべての参照をクリーンアップし、プログラムを送信する必要があります DE 破棄イベントを通知します。|
|[ContinueFromSynchronousEvent](../../../extensibility/debugger/reference/idebugengine2-continuefromsynchronousevent.md)|これまで、SDM を DE によって送信、同期デバッグ イベントが受信され、処理を示す SDM によって呼び出されます。|
|[SetLocale](../../../extensibility/debugger/reference/idebugengine2-setlocale.md)|デのロケールを設定します。|
|[SetRegistryRoot](../../../extensibility/debugger/reference/idebugengine2-setregistryroot.md)|現在、DE が使用してレジストリ ルートを設定します。|
|[SetMetric](../../../extensibility/debugger/reference/idebugengine2-setmetric.md)|メトリックを設定します。|
|[CauseBreak](../../../extensibility/debugger/reference/idebugengine2-causebreak.md)|この DE によってデバッグされているすべてのプログラムが次回実行しようとすると、スレッドの 1 つの実行を停止することを要求します。|

## <a name="requirements"></a>必要条件
 ヘッダー:Msdbg.h

 名前空間: Microsoft.VisualStudio.Debugger.Interop

 アセンブリ:Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>関連項目
- [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)
- [GetEngine](../../../extensibility/debugger/reference/idebugenginecreateevent2-getengine.md)