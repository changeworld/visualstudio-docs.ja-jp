---
title: 空のタイムライン セグメント | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.empty
helpviewer_keywords:
- Concurrency Visualizer, empty timeline segment
ms.assetid: f37b301f-3edc-4e56-8084-feec2dc5a9b1
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 548edc3c069159b0ae55f723a86be4d6fb2fd25f
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56626935"
---
# <a name="empty-timeline-segment"></a>空のタイムライン セグメント
コンカレンシー ビジュアライザーでは、タイムラインのセクションが空になる (白の背景を持つ) の理由は、チャネルの種類によって異なります。

-   CPU スレッド チャネルの場合は、タイムラインのこの部分の間にスレッドが存在しなかったことを意味します。 スレッドについて知りたい場合は、ズーム コントロールまたは水平スクロールを使って、実行セクションを見つけることができます。

-   I/O チャネルの場合は、その時点でターゲット プロセスに対するディスク アクセスが発生しなかったこと意味します。

-   DirectX チャネルの場合は、タイムラインのこの部分の間にターゲット プロセスに対する GPU 処理が実行されなかったことを意味します。

-   マーカー チャネルの場合は、マーカーが生成されなかったことを意味します。

## <a name="see-also"></a>関連項目
- [スレッド ビュー](../profiling/threads-view-parallel-performance.md)
- [ズーム コントロール (スレッド ビュー)](../profiling/zoom-control-threads-view.md)