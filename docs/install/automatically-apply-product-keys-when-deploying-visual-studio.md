---
title: プロダクト キーを自動的に適用する
description: Visual Studio を展開するときに、プロダクト キーをプログラムで適用する方法を説明します。
ms.date: 08/14/2017
ms.custom: seodec18
ms.topic: conceptual
ms.assetid: d79260be-6234-4fd3-89b5-a9756b4a93c1
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0dab3f8f862b27a8124aecf0e19f7649d8b934b7
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/08/2019
ms.locfileid: "55947238"
---
# <a name="automatically-apply-product-keys-when-deploying-visual-studio"></a>Visual Studio の展開時にプロダクト キーを自動的に適用する

Visual Studio の配置を自動化するために使用されるスクリプトの一部として、プログラム的にプロダクト キーを適用することができます。 プロダクト キーは、Visual Studio のインストール中またはインストール完了後に、プログラム的にデバイスで設定できます。

## <a name="apply-the-license-after-installation"></a>インストール後にライセンスを適用する

 ターゲット コンピューターにある `StorePID.exe` ユーティリティをサイレント モードで使用して、インストールされているバージョンの Visual Studio をプロダクト キーでアクティブにすることができます。 `StorePID.exe` は次の既定の場所に Visual Studio 2017 をインストールするユーティリティ プログラムです。 <br> `C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\IDE`

 System Center エージェントまたは管理者特権でのコマンド プロンプトを使用して、昇格された特権で `StorePID.exe` を実行します。 これに続いてプロダクト キーと Microsoft 製品コード (MPC) を入力します。

>[!IMPORTANT]
> プロダクト キーには、ダッシュ (-) を含めてください。

 ```cmd
 StorePID.exe [product key including the dashes] [MPC]
 ```

 次の例は Visual Studio 2017 Enterprise にライセンスを適用するコマンド ラインです。MPC は 08860 で、プロダクト キーは `AAAAA-BBBBB-CCCCC-DDDDDD-EEEEEE` です。既定の場所にインストールするものと想定しています。

 ```cmd
 "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\IDE\StorePID.exe" AAAAA-BBBBB-CCCCC-DDDDDD-EEEEEE 08860
 ```

 次の表に、Visual Studio の各エディションの MPC コードを一覧します。

| Visual Studio エディション                | MPC   |
|--------------------------------------|-------|
| Visual Studio Enterprise 2017        | 08860 |
| Visual Studio Professional 2017      | 08862 |
| Visual Studio Test Professional 2017 | 08866 |

`StorePID.exe` が正常にプロダクト キーを適用した場合は `%ERRORLEVEL%` として 0 を返します。 エラーが発生した場合、エラーの状態に基づいて次のいずれかのコードが返されます。

| Error                     | コード |
|---------------------------|------|
| `PID_ACTION_SUCCESS`      | 0    |
| `PID_ACTION_NOTINSTALLED` | 1    |
| `PID_ACTION_INVALID`      | 2    |
| `PID_ACTION_EXPIRED`      | 3    |
| `PID_ACTION_INUSE`        | 4    |
| `PID_ACTION_FAILURE`      | 5    |
| `PID_ACTION_NOUPGRADE`    | 6    |

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>関連項目

* [Visual Studio のインストール](../install/install-visual-studio.md)
* [Visual Studio のオフライン インストールを作成する](../install/create-an-offline-installation-of-visual-studio.md)
