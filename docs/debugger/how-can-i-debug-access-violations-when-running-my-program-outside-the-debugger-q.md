---
title: デバッガーの外部アプリケーションを実行するときに、アクセス違反をデバッグ |Microsoft Docs
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.access
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- access violation debugging
- debugging [Visual Studio], access violations
ms.assetid: 780a298a-132e-4245-8370-8c82ca27c6c1
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 657d8730f923d144d0691afe921ad5eaf9337a42
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56690046"
---
# <a name="how-can-i-debug-access-violations-when-running-my-program-outside-the-debugger"></a>プログラムの実行中にデバッガーの外部で発生するアクセス違反をデバッグするには

## <a name="problem-description"></a>問題の説明
 プログラムが Visual Studio 環境では正しく動作するのに、Windows オペレーティング システムでスタンドアロンで実行するとアクセス違反が発生します。 どのようにデバッグしたらいいのでしょうか。

## <a name="solution"></a>ソリューション
 [[Just-In-Time デバッグ]](../debugger/just-in-time-debugging-in-visual-studio.md) オプションを設定し、アクセス違反が発生するまでプログラムをスタンドアロンで実行します。 その後、**[アクセス違反です]** ダイアログ ボックスが表示されたら、**[キャンセル]** をクリックしてデバッガーを起動します。

## <a name="see-also"></a>関連項目
- [ネイティブ コードのデバッグに関する FAQ](../debugger/debugging-native-code-faqs.md)
- [ネイティブ コードのデバッグ](../debugger/debugging-native-code.md)