---
title: '方法: SharePoint プロジェクト項目の拡張機能にショートカット メニュー項目の追加 |Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- project items [SharePoint development in Visual Studio], extending
- SharePoint project items, extending
- SharePoint development in Visual Studio, extending project items
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 34c25472b55db39b04b1431e5bdffe8664f79f41
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56621085"
---
# <a name="how-to-add-a-shortcut-menu-item-to-a-sharepoint-project-item-extension"></a>方法: SharePoint プロジェクト項目の拡張機能のショートカット メニュー項目を追加します。
  プロジェクト項目の拡張機能を使用して、既存の SharePoint プロジェクト項目にショートカット メニュー項目を追加できます。 プロジェクト項目を右クリックしたときに、メニュー項目が表示されます**ソリューション エクスプ ローラー**します。

 次の手順では、プロジェクト項目の拡張機能を既に作成したことを前提としています。 詳細については、「[方法 :SharePoint プロジェクト項目の拡張機能作成](../sharepoint/how-to-create-a-sharepoint-project-item-extension.md)です。

### <a name="to-add-a-shortcut-menu-item-in-a-project-item-extension"></a>プロジェクト項目の拡張機能でショートカット メニュー項目を追加するには

1.  <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeExtension.Initialize%2A>のメソッド、<xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeExtension>実装、ハンドル、<xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.ProjectItemMenuItemsRequested>のイベント、 *projectItemType*パラメーター。

2.  イベント ハンドラーで、<xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.ProjectItemMenuItemsRequested>イベントを追加する新しい<xref:Microsoft.VisualStudio.SharePoint.IMenuItem>オブジェクトを<xref:Microsoft.VisualStudio.SharePoint.SharePointProjectItemMenuItemsRequestedEventArgs.ViewMenuItems%2A>または<xref:Microsoft.VisualStudio.SharePoint.SharePointProjectItemMenuItemsRequestedEventArgs.AddMenuItems%2A>イベント引数のパラメーターのコレクション。

3.  <xref:Microsoft.VisualStudio.SharePoint.IMenuItem.Click>新しいイベント ハンドラー<xref:Microsoft.VisualStudio.SharePoint.IMenuItem>オブジェクト、ユーザーがクリックして、ショートカット メニュー項目を実行するタスクを実行します。

## <a name="example"></a>例
 次のコード例では、イベント レシーバー プロジェクト項目にショートカット メニュー項目を追加する方法を示します。 ユーザーが内のプロジェクト項目を右クリックしたとき**ソリューション エクスプ ローラー**クリックして、**出力ウィンドウにメッセージを書き込む**メニュー項目では、Visual Studio でのメッセージが表示されます、**出力**ウィンドウ。

 [!code-vb[SPExtensibility.ProjectItemExtension.MenuAndProperty#1](../sharepoint/codesnippet/VisualBasic/projectitemmenuandproperty/extension/projectitemextensionmenu.vb#1)]
 [!code-csharp[SPExtensibility.ProjectItemExtension.MenuAndProperty#1](../sharepoint/codesnippet/CSharp/projectitemmenuandproperty/extension/projectitemextensionmenu.cs#1)]

 この例では、SharePoint プロジェクト サービスを使用して、メッセージを書き込む、**出力**ウィンドウ。 詳細については、次を参照してください。 [SharePoint プロジェクト サービスを使用して、](../sharepoint/using-the-sharepoint-project-service.md)します。

## <a name="compile-the-code"></a>コードのコンパイル
 この例では、次のアセンブリへの参照を含むクラス ライブラリ プロジェクトが必要です。

-   Microsoft.VisualStudio.SharePoint

-   System.ComponentModel.Composition

## <a name="deploy-the-extension"></a>拡張機能をデプロイします。
 拡張機能を展開するには、作成、[!include[vsprvs](../sharepoint/includes/vsprvs-md.md)]アセンブリおよびその他の拡張機能を配布するファイルの拡張機能 (VSIX) にパッケージ化します。 詳細については、次を参照してください。 [Visual Studio の SharePoint ツールの拡張機能を展開](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md)します。

## <a name="see-also"></a>関連項目
- [方法: SharePoint プロジェクト項目の拡張機能を作成します。](../sharepoint/how-to-create-a-sharepoint-project-item-extension.md)
- [方法: SharePoint プロジェクト項目の拡張機能にプロパティを追加します。](../sharepoint/how-to-add-a-property-to-a-sharepoint-project-item-extension.md)
- [SharePoint プロジェクト項目を拡張します。](../sharepoint/extending-sharepoint-project-items.md)
- [チュートリアル: SharePoint プロジェクト項目の種類を拡張します。](../sharepoint/walkthrough-extending-a-sharepoint-project-item-type.md)
