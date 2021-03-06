---
title: ブレークポイント エラー |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- breakpoints, errors
- debugging [Debugging SDK], breakpoint errors
- errors [Debugging SDK]
ms.assetid: 79221c6b-a924-4c8e-a778-e312e4e0c0c8
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 81f1b484ed3cf34ffd7041b6ff2d72fa6fcb1bf4
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56697118"
---
# <a name="breakpoint-errors"></a>ブレークポイント エラー
次は、ブレークポイントがコードにバインドしようとしたときにプロセスを説明しますが、失敗します。

## <a name="troubleshoot-a-breakpoint-error"></a>ブレークポイント エラーをトラブルシューティングします。

1.  デバッグ エンジン (DE) を送信する[IDebugBreakpointErrorEvent2](../../extensibility/debugger/reference/idebugbreakpointerrorevent2.md)セッション デバッグ マネージャー (SDM)。

2.  SDM コール[IDebugBreakpointErrorEvent2::GetErrorBreakpoint](../../extensibility/debugger/reference/idebugbreakpointerrorevent2-geterrorbreakpoint.md) (IDebugErrorBreakpoint2 * * `ppErrorBP`) エラーのブレークポイントを取得します。

3.  SDM コール[IDebugErrorBreakpoint2::GetPendingBreakpoint](../../extensibility/debugger/reference/idebugerrorbreakpoint2-getpendingbreakpoint.md)エラー ブレークポイントが元の保留中のブレークポイントを取得します。

4.  SDM コール[IDebugErrorBreakpoint2::GetBreakpointResolution](../../extensibility/debugger/reference/idebugerrorbreakpoint2-getbreakpointresolution.md)エラー ブレークポイントがバインドに失敗した理由を取得します。

## <a name="see-also"></a>関連項目
- [デバッガー イベントの呼び出し](../../extensibility/debugger/calling-debugger-events.md)