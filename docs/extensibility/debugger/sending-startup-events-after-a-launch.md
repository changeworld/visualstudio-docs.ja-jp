---
title: 起動の後のスタートアップ イベントの送信 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], startup events
ms.assetid: 306ea0b4-6d9e-4871-8d8d-a4032d422940
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4c9363270593f1d492ec57d119f9a70f8371b0ac
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56685899"
---
# <a name="send-startup-events-after-a-launch"></a>起動の後のスタートアップ イベントを送信します。
デバッグ エンジン (DE) がプログラムにアタッチされると、デバッグ セッションに、一連のスタートアップ イベントを送信します。

 デバッグ セッションに送信されるスタートアップ イベントは次のとおりです。

- エンジンの作成イベントです。

- プログラムの作成イベントです。

- スレッドの作成とモジュール読み込みイベント。

- 読み込み完了イベント、コードが読み込まれ、実行する準備がすべてのコードが実行される前に、送信します。

  > [!NOTE]
  >  このイベントを続行すると、グローバル変数を初期化し、スタートアップ ルーチンを実行します。

- 可能なその他のスレッドの作成とモジュール読み込みイベント。

- 通知プログラムに達したことのメイン エントリ ポイントなどのエントリ ポイント イベント**Main**または`WinMain`します。 通常、このイベントはされていない、DE が既に実行されているプログラムにアタッチする場合に送信されます。

  セッション デバッグ マネージャー (SDM) が最初に送信、DE プログラムで、 [IDebugEngineCreateEvent2](../../extensibility/debugger/reference/idebugenginecreateevent2.md)後に、エンジンの作成イベントを表すインターフェイスを[IDebugProgramCreateEvent2](../../extensibility/debugger/reference/idebugprogramcreateevent2.md)、プログラムの作成イベントを表します。

  これらのイベントは通常 1 つまたは複数後に[IDebugThreadCreateEvent2](../../extensibility/debugger/reference/idebugthreadcreateevent2.md)スレッド作成イベントと[IDebugModuleLoadEvent2](../../extensibility/debugger/reference/idebugmoduleloadevent2.md)モジュール読み込みイベント。

  コードが読み込まれ、実行する準備がデが、SDM を送信するすべてのコードが実行される前に、 [IDebugLoadCompleteEvent2](../../extensibility/debugger/reference/idebugloadcompleteevent2.md)完了イベントをロードします。 最後に、プログラムが既に実行されていない場合、ドイツが送信します。、 [IDebugEntryPointEvent2](../../extensibility/debugger/reference/idebugentrypointevent2.md)エントリ ポイント イベント、通知プログラムのメイン エントリ ポイントに達した、およびデバッグの準備ができています。

## <a name="see-also"></a>関連項目
- [実行の制御](../../extensibility/debugger/control-of-execution.md)
- [タスクのデバッグ](../../extensibility/debugger/debugging-tasks.md)