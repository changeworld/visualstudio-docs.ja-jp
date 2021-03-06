---
title: 並列スタック ウィンドウでスレッドを表示 |Microsoft Docs
ms.date: 11/20/2018
ms.topic: conceptual
f1_keywords:
- vs.debug.parallelstacks
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugger, parallel tasks window
ms.assetid: f50efb78-5206-4803-bb42-426ef8133f2f
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e9728346bc4c6d805bb0febd3a0d5bef0ed809a5
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56712542"
---
# <a name="view-threads-and-tasks-in-the-parallel-stacks-window-c-visual-basic-c"></a>並列スタック ウィンドウのスレッドとタスクの表示 (C#、Visual Basic、C++)

**並列スタック**ウィンドウはマルチ スレッド アプリケーションのデバッグに便利です。 いくつかのビューがあります。

- [スレッド ビュー](#threads-view)アプリのすべてのスレッドの呼び出し履歴情報が表示されます。 スレッドとそれらのスレッドのスタック フレーム間を移動することができます。

- [タスク ビュー](#tasks-view)タスク中心のコール スタック情報が表示されます。
  - マネージ コードで**タスク**の呼び出し履歴を表示します。<xref:System.Threading.Tasks.Task?displayProperty=fullName>オブジェクト。
  - ネイティブ コードで**タスク**の呼び出し履歴を表示します[タスク グループ](/cpp/parallel/concrt/task-parallelism-concurrency-runtime)、[並列アルゴリズム](/cpp/parallel/concrt/parallel-algorithms)、[非同期エージェント](/cpp/parallel/concrt/asynchronous-agents)、および[。軽量タスク](/cpp/parallel/concrt/task-scheduler-concurrency-runtime)します。

- [メソッド ビュー](#method-view)選択したメソッドの呼び出し履歴を回転します。

## <a name="use-the-parallel-stacks-window"></a>[並列スタック] ウィンドウを使用する

開くには、**並列スタック**ウィンドウで、デバッグ セッションである必要があります。 選択**デバッグ** > **Windows** > **並列スタック**します。

### <a name="toolbar-controls"></a>ツール バー コントロール

**並列スタック**ウィンドウには、次のツール バー コントロール。

![並列スタック ウィンドウのツールバー](../debugger/media/parallel_stackstoolbar.png "並列スタック ツールバー")

|アイコン|コントロール|説明|
|-|-|-|
|![スレッド/タスクのコンボ ボックス](media/parallel_toolbar1.png "スレッド/タスクのコンボ ボックス")|**スレッド**/**タスク**コンボ ボックス|スレッドの呼び出し履歴とタスクの呼び出し履歴の表示を切り替えます。 詳細については、「[タスク ビュー](#tasks-view)」および「[スレッド ビュー](#threads-view)」を参照してください。|
|![のみのフラグが設定アイコンを表示する](media/parallel_toolbar2.png "表示のみにフラグが設定されたアイコン")|[フラグが設定されたもののみを表示]|他のデバッガー ウィンドウなどフラグが立てられているスレッドのみの呼び出し履歴が表示されます、 **GPU スレッド**ウィンドウと**並列ウォッチ**ウィンドウ。|
|![切り替えメソッド ビュー アイコン](media/parallel_toolbar3.png "メソッド ビューの切り替えアイコン")|**[メソッド ビュー]** の切り替え|呼び出しスタック ビュー間の切り替えと**メソッド ビュー**します。 詳細については、「[メソッド ビュー](#method-view)」を参照してください。|
|![現在のアイコンを自動的にスクロール](media/parallel_toolbar4.png "現在のアイコンに自動スクロール")|[現在のスタック フレームに自動スクロール]|グラフを自動でスクロールできるように、現在のスタック フレームがビューに表示します。 この機能は、他のウィンドウから現在のスタック フレームを変更した場合、または大規模なグラフで新しいブレークポイントにヒットしたときに便利です。|
|![切り替えのズーム アイコン](media/parallel_toolbar5.png "切り替えのズーム アイコン")|[ズーム コントロールの切り替え]|ウィンドウの左側にあるズーム コントロールの表示と非表示を切り替えます。 <br /><br />ズーム コントロールの可視性に関係なく拡大することもキーを押して**Ctrl**とマウス ホイールまたはでキーを押して**Ctrl**+**Shift** +**+** にズーム インして**Ctrl**+**Shift** + **-** ズーム アウトします。 |

### <a name="stack-frame-icons"></a>スタック フレームのアイコン
次のアイコンは、すべてのビュー内の現在のスタック フレームに関する情報を提供します。

|アイコン|説明|
|-|-|
|![黄色の矢印](media/icon_parallelyellowarrow.gif)|現在のスレッドの現在の場所 (アクティブなスタック フレーム) を示します。|
|![スレッドのアイコン](media/icon_parallelthreads.gif)|現在ではないスレッドの現在の場所 (アクティブなスタック フレーム) を示します。|
|![緑色の矢印](media/icon_parallelgreenarrow.gif)|現在のスタック フレーム (現在のデバッガー コンテキスト) を示します。 メソッド名が太字表示される任意の場所です。|

### <a name="context-menu-items"></a>コンテキスト メニュー項目
内のメソッドを右クリックすると、次のショートカット メニュー項目が利用**スレッド**ビューまたは**タスク**ビュー。 最後の 6 つの項目がの場合と同じ、[呼び出し履歴 ウィンドウ](how-to-use-the-call-stack-window.md)します。

![並列スタック ウィンドウのショートカット メニュー](../debugger/media/parallel_contmenu.png "並列スタック ウィンドウのショートカット メニュー")

|メニュー項目|説明|
|-|-|
|**フラグ**|選択した項目にフラグを設定します。|
|**フラグ解除**|選択した項目のフラグを解除します。|
|**凍結**|選択した項目を凍結します。|
|**解凍**|選択した項目の凍結を解除します。|
|**フレームに切り替え**|対応するメニューと同じコマンドを**呼び出し履歴**ウィンドウ。 ただしでは、**並列スタック**ウィンドウで、1 つのメソッドは、複数のフレームにする可能性があります。 この項目のサブメニューで、目的のフレームを選択できます。 現在のスレッドのスタック フレームのいずれかの場合、そのフレームはサブメニューに既定で選択されます。|
|**タスクに移動して**または**スレッドに移動**|切り替わり、**タスク**または**スレッド**ビュー、および同じのスタック フレームが強調表示を保持します。|
|**ソース コードへ移動**|ソース コード ウィンドウ内の対応する場所に移動します。 |
|**逆アセンブルを表示**|対応する場所に移動、**逆アセンブル**ウィンドウ。|
|**外部コードの表示**|外部コードの表示と非表示を切り替えます。|
|**16 進数で表示**|10 進数と 16 進数の表示を切り替えます。|
|**ソースのスレッドを表示**|ソース コード ウィンドウ内のスレッドの場所のフラグを設定します。 |
|**シンボルの読み込み情報**|開く、**シンボルの読み込み情報** ダイアログ ボックス。|
|**シンボルの設定**|開く、**シンボル設定** ダイアログ ボックス。 |

## <a name="threads-view"></a>スレッド ビュー

**スレッド**スタック フレームを表示して、現在のスレッドの呼び出しパスは青で強調表示されます。 スレッドの現在の場所は、黄色の矢印で表示されます。

現在のスタック フレームを変更するには、別の方法をダブルクリックします。 また、かどうか、現在のスレッドまたは別のスレッドの一部は、選択した方法に応じて、現在のスレッドを切り替えるこの可能性があります。

ときに、**スレッド**、ウィンドウに収まるようにグラフの表示が大きすぎて、**バード アイ ビュー**  ウィンドウでコントロールが表示されます。 グラフのさまざまな部分に移動するコントロールでは、フレームを移動できます。

次の図は、ネイティブ コードへの切り替えにマネージに Main から移動する 1 つのスレッドを示します。 6 つのスレッドでは、現在のメソッドです。 Thread.Sleep、1 つは引き続きし、Console.WriteLine し SyncTextWriter.WriteLine 別が続行されます。

 ![並列スタック ウィンドウのビューをスレッド](../debugger/media/parallel_stack1.png "スレッド並列スタック ウィンドウ ビュー")

次の表の主な機能、**スレッド**ビュー。

|引き出し線|[要素名]|説明|
|-|-|-|
|1|呼び出し履歴のセグメントまたはノード|一連メソッドの 1 つまたは複数のスレッドにはが含まれています。 それに接続されている矢印の線、フレームがない場合は、フレームは、スレッドのすべての呼び出しパスを示します。|
|2|青の強調表示|現在のスレッドの呼び出しパスを示します。|
|3|矢印の線|ノードを結び、スレッドのすべての呼び出しパスを構成します。|
|4|ノードのヘッダー|プロセスとノードのスレッドの数を示します。|
|5|メソッド|同じメソッド内の 1 つ以上のスタック フレームを表します。|
|6|メソッドのツールヒント|メソッドを合わせると表示されます。 **スレッド**のようなテーブルでビュー、ツールヒントの表示、すべてのスレッド、**スレッド**ウィンドウ。 |

## <a name="tasks-view"></a>タスク ビュー
アプリで使用する場合<xref:System.Threading.Tasks.Task?displayProperty=fullName>オブジェクト (マネージ コード) または`task_handle`使用する並列処理を表現するオブジェクト (ネイティブ コード)、**タスク**ビュー。 **タスク** ビューには、スレッドではなくタスクの呼び出し履歴が表示されます。

**タスク**ビュー。

- タスクを実行していないスレッドの呼び出し履歴は表示されません。
- タスクを実行しているスレッドの呼び出し履歴が上部と下部にある、タスクの最も重要なフレームを表示する視覚的にトリミングされます。
- いくつかのタスクは、1 つのスレッドでは、個別のノードでこれらのタスクの呼び出し履歴が表示されます。

すべての呼び出し履歴を表示に切り替えます**スレッド**のスタック フレームを右クリックしてビュー**スレッドに移動**します。

次の図は、**スレッド**最上部にあり、対応するビュー**タスク**下部に表示します。

![スレッドおよびタスク ビュー](../debugger/media/parallel_threads-tasks.png "スレッドとタスク ビュー")

追加情報を含むヒントを表示するメソッドをポイントします。 **タスク**ビュー、ツールヒントのすべてのタスク テーブルに表示のような**タスク**ウィンドウ。

次の図は、メソッドのツールヒント、**スレッド**ビューの上部にあると、対応する**タスク**下部に表示します。

![スレッドとタスクのツールヒント](../debugger/media/parallel_threads-tasks-tooltips.png "スレッドとタスクのツールヒント")

## <a name="method-view"></a>メソッド ビュー
いずれかから**スレッド**ビューまたは**タスク**ビューを選択して、現在のメソッドのグラフをピボットすることができます、**メソッド ビューの切り替え**ツールバーのアイコン。 **メソッド ビュー**を使用すると、現在のメソッドを呼び出すか現在のメソッドから呼び出されるすべてのスレッドのすべてのメソッドをひと目で確認できます。 次の図で、同じ情報を表示する方法を示しています。**スレッド**表示上、左と**メソッド ビュー**右側の。

![スレッド ビューとメソッド ビュー](../debugger/media/parallel_methodview.png "スレッド ビューとメソッド ビュー")

現在のメソッドは、メソッドが行う場合は、新しいスタック フレームに切り替えると、および**メソッド ビュー**すべての呼び出し元と、新しいメソッドの呼び出し先を示します。 これにより、そのメソッドが呼び出し履歴に含まれているかどうかに応じて、一部のスレッドの表示と非表示が切り替わる場合があります。 呼び出し履歴のビューに戻るに、選択、**メソッド ビュー**ツール バー アイコンをもう一度です。

## <a name="see-also"></a>関連項目
- [マルチ スレッド アプリケーションのデバッグの開始します。](../debugger/get-started-debugging-multithreaded-apps.md)
- [チュートリアル: 並行アプリケーションをデバッグする](../debugger/walkthrough-debugging-a-parallel-application.md)
- [デバッガーでのはじめに](../debugger/debugger-feature-tour.md)
- [マネージド コードをデバッグする](../debugger/debugging-managed-code.md)
- [並列プログラミング](/dotnet/standard/parallel-programming/index)
- [[タスク] ウィンドウを使用する](../debugger/using-the-tasks-window.md)
- [Task クラス](../extensibility/debugger/task-class-internal-members.md)
