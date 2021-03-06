---
title: '方法: ClickOnce アプリケーションの既定の Web ページをカスタマイズする |Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- Publish.htm Web page
- ClickOnce deployment default Web page
- deploying applications [ClickOnce], publishing
- publishing, ClickOnce
ms.assetid: 418de18c-bee9-4f24-9cd9-0252d175070d
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9831c1176b5e71650742226e77bfca58dfa35a01
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56608446"
---
# <a name="how-to-customize-the-default-web-page-for-a-clickonce-application"></a>方法: ClickOnce アプリケーションの既定の Web ページをカスタマイズする
ClickOnce アプリケーションの Web を発行するときに、Web ページが自動的に生成され、アプリケーションと共に発行します。 既定のページには、アプリケーションとアプリケーションのインストール、インストールの前提条件、または MSDN のヘルプにアクセスするリンクの名前が含まれています。

> [!NOTE]
>  ページに表示される実際のリンクは、ページが表示されているコンピューターとによって異なります。 前提条件が含まれています。

 Web ページの既定の名前は*Publish.htm*; 内の名前を変更することができます、**プロジェクト デザイナー**します。 詳細については、次を参照してください。[方法: ClickOnce アプリケーションの発行ページ指定](../deployment/how-to-specify-a-publish-page-for-a-clickonce-application.md)します。

 *Publish.htm* Web ページの新しいバージョンが検出された場合にのみ公開されます。

> [!NOTE]
>  対して行った変更、**発行**設定は影響しません、 *Publish.htm*  ページで、1 つの例外: 前提条件の一覧には追加の前提条件を最初に発行した後に削除するか、できなきます。 変更を反映する前提条件となるリンクのテキストを編集する必要があります。

### <a name="to-customize-the-publish-web-page"></a>発行 Web ページをカスタマイズするには

1.  Web 上の場所に、ClickOnce アプリケーションを発行します。 詳細については、次を参照してください。[方法: 発行ウィザードを使用して ClickOnce アプリケーションを発行](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)します。

2.  Web サーバーで開く、 *Publish.htm* Visual Web Designer または別の HTML エディターでファイル。

3.  必要に応じて、ページをカスタマイズし、保存します。

4.  任意。 Visual Studio の発行のカスタマイズされた Web ページの上書きを防ぐためにオフにします。**後に配置 Web ページを自動的に生成すべて発行**で、**発行オプション** ダイアログ ボックス。

## <a name="see-also"></a>関連項目
- [ClickOnce のセキュリティと配置](../deployment/clickonce-security-and-deployment.md)
- [ClickOnce アプリケーションの発行](../deployment/publishing-clickonce-applications.md)
- [方法: ClickOnce アプリケーションと共に必須コンポーネントをインストールする](../deployment/how-to-install-prerequisites-with-a-clickonce-application.md)
- [方法: ClickOnce アプリケーションの発行ページを指定する](../deployment/how-to-specify-a-publish-page-for-a-clickonce-application.md)