---
title: ClickOnce 配置ストラテジの選択 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce deployment, strategies
- deploying applications, ClickOnce
ms.assetid: 98bcab65-ab8b-4ed1-9adc-fdacf92b8106
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0198c9e9e6238547bb8a9ea1a49c9f8a2a611cbc
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56603977"
---
# <a name="choose-a-clickonce-deployment-strategy"></a>ClickOnce 配置ストラテジの選択
[!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] アプリケーションを配置する際には 3 つのストラテジがあり、どれを選択するかは主として配置するアプリケーションの種類によって決まります。 この 3 つの配置ストラテジは次のとおりです。

-   Web またはネットワーク共有からのインストール

-   CD からのインストール

-   Web またはネットワーク共有からのアプリケーションの起動

    > [!NOTE]
    >  配置ストラテジを選択するだけでなく、アプリケーションの更新プログラムを提供するストラテジも選択する必要があります。 詳細については、次を参照してください。 [ClickOnce の更新方法の選択](../deployment/choosing-a-clickonce-update-strategy.md)します。

## <a name="install-from-the-web-or-a-network-share"></a>Web またはネットワーク共有からのインストール
 このストラテジを使用すると、アプリケーションが Web サーバーまたはネットワーク ファイル共有に配置されます。 エンド ユーザーがアプリケーションをインストールするときは、Web ページのアイコンをクリックするか、ファイル共有のアイコンをダブルクリックします。 これで、アプリケーションがユーザーのコンピューターにダウンロードされ、インストールされて起動します。 項目が **[スタート]** メニューと **[コントロール パネル]** の **[プログラムの追加と削除]** に追加されます。

 このストラテジはネットワーク接続に依存するため、ローカル エリア ネットワークや高速インターネット接続にアクセスできるユーザーのコンピューターにアプリケーションを配置する場合に最適です。

 アプリケーションを Web から配置する場合は、そのアプリケーションが URL を使用してアクティブ化されるときに、アプリケーションに引数を渡すことができます。 詳細については、次を参照してください。[方法: オンライン ClickOnce アプリケーションでは、クエリ文字列の情報を取得](../deployment/how-to-retrieve-query-string-information-in-an-online-clickonce-application.md)します。 ここで説明されている他の方法でアクティブ化されるアプリケーションには、引数を渡すことができません。

 この配置ストラテジを [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] で有効にするには、発行ウィザードの **[ユーザーはアプリケーションをどのようにインストールするのですか?]** ページで **[Web サイトから]** または **[UNC パスまたはファイル共有から]** をクリックします。

 これは既定の配置ストラテジです。

## <a name="start-the-application-from-the-web-or-a-network-share"></a>Web またはネットワーク共有からのアプリケーションの起動
 このストラテジは 1 番目のストラテジに似ていますが、アプリケーションが Web アプリケーションのように動作する点が異なります。 ユーザーが Web ページのリンクをクリック (またはファイル共有のアイコンをダブルクリック) すると、アプリケーションが起動します。 ユーザーがアプリケーションを閉じると、アプリケーションはユーザーのローカル コンピューターで使用できなくなり、**[スタート]** メニューや **[コントロール パネル]** の **[プログラムの追加と削除]** には何も追加されません。

> [!NOTE]
>  厳密には、アプリケーションは、Web アプリケーションが Web キャッシュにダウンロードされるのと同様に、ローカル コンピューターのアプリケーション キャッシュにダウンロードされ、インストールされます。 Web キャッシュの場合と同様に、ファイルは最終的にアプリケーション キャッシュから削除されます。 ただし、ユーザーの目には、アプリケーションが Web またはファイル共有から実行されるように映ります。

 このストラテジは、使用頻度の低いアプリケーション (通常、年に 1 回しか実行されない従業員福利ツールなど) に最適です。

 この配置ストラテジを [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] で有効にするには、発行ウィザードの **[アプリケーションはオフラインでも利用できますか?]** ページで **[いいえ、このアプリケーションはオンラインでのみ利用できます]** をクリックします。

 この配置ストラテジを手動で有効にするには、配置マニフェストの **install** タグを変更します。 (その値は **true** または **false** になります。 *Mage.exe* では、**[アプリケーションの種類]** リストの **[オンラインのみ]** を使用します。)

## <a name="install-from-a-cd"></a>CD からのインストール
 このストラテジを使用すると、CD-ROM や DVD などのリムーバブル メディアにアプリケーションが配置されます。 前のオプションと同様に、ユーザーがアプリケーションのインストールを選択すると、アプリケーションがインストールされて起動し、関連項目が **[スタート]** メニューと **[コントロール パネル]** の **[プログラムの追加と削除]** に追加されます。

 このストラテジは、永続的なネットワーク接続を利用していないユーザーや低帯域幅接続を利用しているユーザーに対してアプリケーションを配置する場合に最適です。 アプリケーションはリムーバブル メディアからインストールするため、インストールの際にネットワーク接続は不要ですが、アプリケーションの更新には、ネットワーク接続が必要です。

 この配置ストラテジを [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] で有効にするには、発行ウィザードの **[ユーザーはアプリケーションをどのようにインストールするのですか?]** ページで **[CD-ROM または DVD-ROM から]** をクリックします。

 この配置ストラテジを手動で有効にするには、配置マニフェストの **deploymentProvider** タグを変更します。 (Visual Studio では、このプロパティはプロジェクト デザイナーの **[発行]** ページの **[インストールの URL]** として公開されます。 *Mage.exe* では、**[Start Location]** です。)

## <a name="web-browser-support"></a>Web ブラウザー サポート
 .NET Framework 3.5 を対象とするアプリケーションは、任意のブラウザーを使用してインストールできます。

 .NET Framework 2.0 を対象とするアプリケーションは、Internet Explorer が必要です。

## <a name="see-also"></a>関連項目
- [ClickOnce のセキュリティと配置](../deployment/clickonce-security-and-deployment.md)
- [ClickOnce の更新方法の選択](../deployment/choosing-a-clickonce-update-strategy.md)
- [方法: 発行ウィザードを使用して ClickOnce アプリケーションの発行](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)
- [ClickOnce アプリケーションのセキュリティ保護](../deployment/securing-clickonce-applications.md)