---
title: COM サーバーおよびコンテナーのデバッグ |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.com
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- ActiveX control container debugging [Visual Studio]
- debugging ActiveX controls
- COM servers, debugging
- ActiveX controls, debugging
- COM [Visual Studio], debugging
ms.assetid: b7ce8696-ebb8-4354-a767-f76b8ada4ac1
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 104af46114da44d3d4a4348e760bd24a2aab5412
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56602053"
---
# <a name="com-server-and-container-debugging"></a>COM サーバーおよび COM コンテナーのデバッグ
COM アプリケーションは、プログラマが直接コントロールできないところで多くのタスクを実行します。 DLL 間の通信、オブジェクトの使用数のカウント、クリップボード処理などは、予期せぬ動作に遭遇する領域のほんの一例です。 このような事態が発生した場合は、まず問題の原因を追及します。

 Visual Studio のデバッガーは、コンテナーやサーバー間のステップやステップ インをサポートしています。 この機能には、リモート プロシージャ コール (RPC) 間のステップも含まれます。

##  <a name="BKMK_COMServerandContainerintheSameSolution"></a> 同じソリューション内の COM サーバーおよび COM コンテナーのデバッグ
 同じソリューションで 2 つのプロジェクトを使用して、COM サーバーおよび COM コンテナーをデバッグできます。 それぞれのプロジェクトに適切なブレークポイントを設定してデバッグを行います。 ブレークポイントが設定されているサーバーをコンテナーが呼び出すと、サーバーのコードに戻るまで、つまりデバッグが終了するまで、コンテナーは待機しています。

 COM コンテナーのデバッグは、標準的なプログラムのデバッグによく似ています。 違いがあるのは、コンテナー アプリケーションにデータをドラッグするなど、コールバックを生成するイベントをデバッグする場合です。 この場合は、ブレークポイントをコールバック関数の中に設定する必要があります。

##  <a name="BKMK_ServerApplicationWithoutContainerInformation"></a> コンテナー情報のないサーバー アプリケーションのデバッグ
 コンテナー アプリケーションのデバッグ情報が不要な場合、サーバー アプリケーションは次の 3 つの手順でデバッグします。

1.  サーバーのデバッグを通常のアプリケーションと同様に開始します。

2.  必要な場所にブレークポイントを設定します。

3.  コンテナー アプリケーションを起動します。

##  <a name="BKMK_DebuggingaServerandDomainIsolationSDIApplication"></a> サーバーとドメインの分離 (SDI) アプリケーションのデバッグ
 SDI サーバー アプリケーションをデバッグする場合は、C/C++、C#、または Visual Basic のプロジェクトの [*プロジェクト* プロパティ ページ] ダイアログ ボックスで、**[コマンド ライン引数]** プロパティに `/Embedding` または `/Automation` を指定する必要があります。

 デバッガーはこれらのコマンド ライン引数を利用して、コンテナーから起動されたようにサーバー アプリケーションを起動できます。 次に、プログラム マネージャーまたはファイル マネージャーからコンテナーを起動すると、コンテナーはデバッガー中で起動されたサーバーのインスタンスを使用できます。

 [*プロジェクト* プロパティ ページ] ダイアログ ボックスにアクセスするには、ソリューション エクスプローラーでプロジェクトを右クリックし、ショートカット メニューの [プロパティ] を選びます。 [コマンド ライン引数] プロパティを表示するには、[構成プロパティ] カテゴリを展開し、[デバッグ] ページをクリックします。

## <a name="see-also"></a>関連項目

- [COM および ActiveX のデバッグ](../debugger/com-and-activex-debugging.md)