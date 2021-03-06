---
title: 実行対象の C++ 規則を指定する設定ルールを使用して |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: ac3877e6-5349-4c03-9541-3d5be259f1e8
caps.latest.revision: 7
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 42c8926403825032f295c31e2ce113bef4ff1bbd
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2018
ms.locfileid: "51810282"
---
# <a name="using-rule-sets-to-specify-the-c-rules-to-run"></a>規則セットを使用した実行対象の C++ 規則の指定
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[!INCLUDE[vsPreShort](../includes/vspreshort-md.md)]と[!INCLUDE[vsUltShort](../includes/vsultshort-md.md)]、作成して、カスタムの変更*ルール セット*コード分析に関連付けられている特定のプロジェクトのニーズを満たします。 カスタムの C++ 規則を作成するのには、C と C++ プロジェクトが Visual Studio IDE で開く必要があります。 規則セット エディターで、標準の規則セットを開くと、追加または特定の規則を削除し、必要に応じて変更コード分析ルールに違反したことを決定するときに発生するアクション。  
  
 新規のカスタム規則セットを作成する場合は、新しいファイル名を使用して保存します。 作成したカスタム規則セットは、自動的にプロジェクトに割り当てられます。  
  
## <a name="opening-the-rule-set-editor"></a>規則セット エディターを開く  
  
#### <a name="to-create-a-custom-rule-from-a-single-existing-rule-set"></a>既存の 1 つの規則セットからカスタム規則を作成するには  
  
1. ソリューション エクスプ ローラーで プロジェクトのショートカット メニューを開き、**プロパティ**します。  
  
2. **プロパティ** タブで、選択**コード分析**します。  
  
3. **ルール セットの**ドロップダウン リストで、次のいずれかの操作を行います。  
  
   - 規則セットをカスタマイズするを選択します。  
  
     \- または -  
  
   - 選択 **\<[参照...] >** を既存の規則セットを指定されていないリスト。  
  
4. 選択**オープン**ルール セット エディターで、ルールを表示します。  
  
#### <a name="to-modify-a-rule-set-in-the-rule-set-editor"></a>規則セット エディターで規則セットを変更するには  
  
-   ルール セットの表示名を変更する、**ビュー**  メニューの 選択**プロパティ ウィンドウ**します。 表示名を入力、**名前**ボックス。 表示名には、ファイル名と異なる名前を指定できます。  
  
-   グループ内のすべての規則をカスタム規則セットに追加するには、グループのチェック ボックスをオンにします。 グループ内のすべての規則を削除するには、チェック ボックスをオフにします。  
  
-   特定の規則をカスタム規則セットに追加するには、その規則のチェック ボックスをオンにします。 規則セットから規則を削除するには、チェック ボックスをオフにします。  
  
-   コード分析のルールに違反したときの動作を変更するには、選択、**アクション**規則のフィールドし、次の値のいずれかを選択します。  
  
     **警告**-警告が生成されます。  
  
     **エラー** -エラーが生成されます。  
  
     **None** -ルールを無効にします。 このアクションは、規則セットから規則を削除するのと同じです。  
  
#### <a name="to-group-filter-or-change-the-fields-in-the-rule-set-editor-by-using-the-rule-set-editor-toolbar"></a>規則セット エディターのツール バーを使用して、規則セット エディターに表示されるフィールドのグループ化、フィルター処理、または変更を行うには  
  
-   すべてのグループの規則を展開するには、選択**すべて展開**します。  
  
-   すべてのグループの規則を折りたたむには、次のように選択します。**すべて折りたたみ**します。  
  
-   ルールは別にグループ化フィールドを変更するからフィールドを選択、 **Group By**一覧。 グループに属していないルールを表示するには、次のように選択します。  **\<None >** します。  
  
-   追加または列のルールでフィールドを削除、選択**列オプション**します。  
  
-   現在のソリューションに適用されない規則を非表示にするには、 **、現在のソリューションに適用されない規則を非表示に**します。  
  
-   表示とエラーのアクションが割り当てられているルールを非表示の切り替え、次のように選択します。**コード分析エラーを生成するルールを表示する**します。  
  
-   表示と警告の動作が割り当てられているルールを非表示の切り替え、次のように選択します。**コード分析の警告を生成するルールを表示する**します。  
  
-   表示と割り当てられているルールを非表示を切り替える、 **None**アクション、選択**が有効になっていないルールが表示されます**します。  
  
-   追加または Microsoft の現在のルール セットの既定の規則セットを削除、選択**子規則セットの追加または削除する**します。



