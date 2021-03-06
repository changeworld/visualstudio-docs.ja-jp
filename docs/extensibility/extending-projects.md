---
title: プロジェクトの拡張 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- solutions [Visual Studio]
- projects [Visual Studio]
ms.assetid: 096d273d-4fe9-4f24-9b00-470bfbdf4bdf
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d31da41e3be73f4e2e036841bfc1d96f4476e856
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56695415"
---
# <a name="extend-projects"></a>プロジェクトを拡張します。
プロジェクトおよびソリューションは、Visual Studio コードとリソース ファイルをコンパイルおよび展開の単位に整理する方法です。 プロジェクトの詳細については見つかります[プロジェクト (Visual Studio SDK)](../extensibility/extending-projects.md)します。

 独自のプロジェクトの種類を作成するには、Visual Studio SDK をダウンロードできるプロジェクトでは、Managed Package Framework[プロジェクト用 Managed Package Framework](https://github.com/tunnelvisionlabs/MPFProj10)します。 理解するカスタム プロジェクトは、実装方法を参照してください。[新しいプロジェクトの生成。内部的には、パート 1](../extensibility/internals/new-project-generation-under-the-hood-part-one.md)と[新しいプロジェクトの生成。内部的には、2 つのパート](../extensibility/internals/new-project-generation-under-the-hood-part-two.md)します。

 このセクションのトピックでは、カスタムのプロジェクトを作成する方法とさまざまな種類の Visual Studio ソリューションを管理する方法について説明します。

## <a name="in-this-section"></a>このセクションの内容
- [基本的なプロジェクト システム、第 1 部作成](../extensibility/creating-a-basic-project-system-part-1.md)カスタム プロジェクト システムを作成する方法について説明します。

- [基本的なプロジェクト システム、第 2 部作成](../extensibility/creating-a-basic-project-system-part-2.md)カスタム プロジェクト システムを作成する方法について説明します。

- [プロジェクト ファイルにデータを保存](../extensibility/saving-data-in-project-files.md)問題について説明がプロジェクトに追加する方法 (<em>.</em>proj *) ファイル。

- [実行時に、プロジェクトのサブタイプを確認します。](../extensibility/verifying-subtypes-of-a-project-at-run-time.md)実行時に、プロジェクトのサブタイプであることを確認する方法について説明します。

- [追加および削除のプロパティ ページ](../extensibility/adding-and-removing-property-pages.md)カスタム プロジェクトのプロパティ ページをカスタマイズする方法について説明します。

- [プロジェクト項目に属性を追加](../extensibility/adding-an-attribute-to-a-project-item.md)カスタム プロジェクト項目に属性を追加する方法について説明します。

- [プロジェクト項目のプロパティを永続化](../extensibility/persisting-the-property-of-a-project-item.md)カスタム プロジェクト項目のプロパティを永続化する方法について説明します。

- [ユニバーサル Windows プロジェクト管理](../extensibility/managing-universal-windows-projects.md)ユニバーサル プロジェクトを管理する方法について説明します。