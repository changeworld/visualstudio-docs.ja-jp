---
title: IDebugBoundBreakpoint2 |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugBoundBreakpoint2
helpviewer_keywords:
- IDebugBoundBreakpoint2 interface
ms.assetid: df33c52e-ded2-48a0-951d-1f36c8fc922e
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f31676cb112dc6e5c7cfe45dcab36893ddb38033
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2018
ms.locfileid: "51773393"
---
# <a name="idebugboundbreakpoint2"></a>IDebugBoundBreakpoint2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

このインターフェイスは、コードの場所にバインドされているブレークポイントを表します。  
  
## <a name="syntax"></a>構文  
  
```  
IDebugBoundBreakpoint2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>実装についてのメモ  
 デバッグ エンジン (DE) は、ブレークポイントのサポートの一部として、このインターフェイスを実装します。  
  
## <a name="notes-for-callers"></a>呼び出し元のノート  
 呼び出し[バインド](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md)このインターフェイスを作成します。 呼び出し[GetBreakpoint](../../../extensibility/debugger/reference/idebugbreakpointunboundevent2-getbreakpoint.md)と[次](../../../extensibility/debugger/reference/ienumdebugboundbreakpoints2-next.md)このインターフェイスを取得することもできます。  
  
## <a name="methods-in-vtable-order"></a>Vtable 順序のメソッド  
 次の表は、メソッドの`IDebugBoundBreakpoint2`します。  
  
|メソッド|説明|  
|------------|-----------------|  
|[GetPendingBreakpoint](../../../extensibility/debugger/reference/idebugboundbreakpoint2-getpendingbreakpoint.md)|指定されたバインドされたブレークポイントの作成元となる保留中のブレークポイントを取得します。|  
|[GetState](../../../extensibility/debugger/reference/idebugboundbreakpoint2-getstate.md)|このバインドされたブレークポイントの状態を取得します。|  
|[GetHitCount](../../../extensibility/debugger/reference/idebugboundbreakpoint2-gethitcount.md)|このバインドされたブレークポイントの現在のヒット カウントを取得します。|  
|[GetBreakpointResolution](../../../extensibility/debugger/reference/idebugboundbreakpoint2-getbreakpointresolution.md)|このブレークポイントを表すブレークポイント解像度を取得します。|  
|[Enable](../../../extensibility/debugger/reference/idebugboundbreakpoint2-enable.md)|有効または、ブレークポイントを無効にします。|  
|[SetHitCount](../../../extensibility/debugger/reference/idebugboundbreakpoint2-sethitcount.md)|このバインドされたブレークポイントのヒット カウントを設定します。|  
|[SetCondition](../../../extensibility/debugger/reference/idebugboundbreakpoint2-setcondition.md)|設定またはバインドされたこのブレークポイントに関連付けられている条件を変更します。|  
|[SetPassCount](../../../extensibility/debugger/reference/idebugboundbreakpoint2-setpasscount.md)|このバインドされたブレークポイントに関連付けられているパスの数を変更または設定します。|  
|[削除](../../../extensibility/debugger/reference/idebugboundbreakpoint2-delete.md)|ブレークポイントを削除します。|  
  
## <a name="requirements"></a>必要条件  
 ヘッダー: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 アセンブリ: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>関連項目  
 [GetBreakpoint](../../../extensibility/debugger/reference/idebugbreakpointunboundevent2-getbreakpoint.md)   
 [次に](../../../extensibility/debugger/reference/ienumdebugboundbreakpoints2-next.md)   
 [Bind](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md)

