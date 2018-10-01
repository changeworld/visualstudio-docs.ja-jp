---
title: コンパートメント シェイプのプロパティ |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.dsltools.dsldesigner.compartmentshape
helpviewer_keywords:
- Domain-Specific Language, compartment shape
ms.assetid: 9a9e112d-210d-413b-a44f-0e976a4a78bc
caps.latest.revision: 26
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 8ae8a384fd554185c35abe007472decbe2d91242
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/22/2018
ms.locfileid: "47535354"
---
# <a name="properties-of-compartment-shapes"></a>コンパートメント シェイプのプロパティ
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

このトピックの最新バージョンをご覧[コンパートメント シェイプのプロパティの](https://docs.microsoft.com/visualstudio/modeling/properties-of-compartment-shapes)します。  
  
コンパートメント シェイプには、ドメイン固有言語におけるドメイン クラスを表示する図形の 1 つがあります。 展開し、コンパートメントを折りたたむことができます。  
  
 詳細については、次を参照してください。[ドメイン固有言語を定義する方法](../modeling/how-to-define-a-domain-specific-language.md)します。 これらのプロパティを使用する方法の詳細については、次を参照してください。[をカスタマイズすると、ドメイン固有言語を拡張する](../modeling/customizing-and-extending-a-domain-specific-language.md)します。  
  
 コンパートメント シェイプには、次の表に記載されているプロパティがあります。  
  
|プロパティ|説明|既定値|  
|--------------|-----------------|-------------|  
|既定値は、折りたたみの状態を展開します。|場合`Expanded`コンパートメントは作成時に表示されます。 場合`Collapsed`、いません。|展開済み|  
|[塗りつぶしの色]|この図形の塗りつぶしの色。|白|  
|塗りつぶしのグラデーション モード|この図形の塗りつぶしのグラデーション モード。|[水平方向]|  
|geometry|この図形 (四角形または角丸長方形) のジオメトリ。|四角形|  
|既定の接続ポイントします。|場合`True`図形を使用して、top、bottom、left、および右の接続は、生成されたデザイナーで参照します。|False|  
|1 つのコンパートメントのヘッダーの表示|場合`False`図形に 1 つのコンパートメントがあるとは、コンパートメントのヘッダーは表示されません。|True|  
|アウトラインの色|この図形のアウトラインの色。|黒|  
|輪郭の実線/点線スタイル|(実線、破線、ドット、DashDot、DashDotDot、カスタム) は、この図形の輪郭の実線/点線スタイル。|[実線]|  
|外枠の太さ|この図形のアウトラインの太さです。|0.03125|  
|テキストの色|この図形に関連付けられているテキスト デコレーターに使用する色。|黒|  
|アクセス修飾子|コンパートメント シェイプへのアクセスのレベル (`public`または`internal`)。|Public|  
|カスタム属性|このコンパートメント シェイプから生成されるソース コードのクラスに属性を追加するために使用|\<なし >|  
|Double 型を生成します派生。|場合`True`、基底クラスと (オーバーライドによってカスタマイズをサポート) する部分クラスの両方が生成されます。 詳細については、次を参照してください。[をオーバーライドすると、生成されたクラスを拡張する](../modeling/overriding-and-extending-the-generated-classes.md)します。|False|  
|カスタム コンス トラクターがあります。|場合`True`、カスタム コンス トラクターは、ソース コードで提供されます。 詳細については、次を参照してください。[をオーバーライドすると、生成されたクラスを拡張する](../modeling/overriding-and-extending-the-generated-classes.md)します。|False|  
|継承修飾子|コンパートメント シェイプから生成されるソース コードのクラスの継承の種類について説明します (`none`、`abstract`または`sealed`)。|なし|  
|基本のコンパートメント シェイプ|この図形の基本クラス。|(なし)|  
|名前|この図形の名前。|現在の名前|  
|名前空間|この図形に関連付ける名前空間。|現在の名前空間|  
|ツールヒントの種類|(固定、変数、またはなし)、ツールヒントを定義する方法。 、しの値を固定する場合、`Fixed Tooltip Text`プロパティ、ツール ヒントとして使用されます。 変数の場合、ツールヒントがカスタム コードで定義します。|none|  
|メモ|この図形に関連付けられている非公式のメモ。|\<なし >|  
|初期の高さ|インチ単位で、この図形の初期の高さ。 コンパートメント図形の場合は、これは、ヘッダー セクションのみの高さとサイズを変更できません。|1|  
|初期の幅|インチ単位で、この図形の初期の幅。|1.5|  
|プロパティとして公開されている塗りつぶしの色<br /><br /> 公開された塗りつぶしのグラデーション モード<br /><br /> アウトラインの色をプロパティとして公開<br /><br /> 輪郭の実線/点線スタイルをプロパティとして公開<br /><br /> アウトラインの太さのプロパティとして公開されています。<br /><br /> テキストの色を公開します。|場合`True`図形の規定されたプロパティを設定できます。 この設定は、シェイプの定義を右クリックし、クリックして**公開追加**します。|False|  
|説明|生成されたデザイナーを文書化するために使用します。|\<なし >|  
|表示名|この図形に生成されたデザイナーに表示される名前です。|\<なし >|  
|固定のツールヒント テキスト|固定のツールヒントに使用されるテキスト。|\<なし >|  
|ヘルプ キーワード|この図形の F1 ヘルプのインデックスを作成するために使用するキーワードです。|\<なし >|  
  
## <a name="see-also"></a>関連項目  
 [ドメイン固有言語ツールの用語集](http://msdn.microsoft.com/en-us/ca5e84cb-a315-465c-be24-76aa3df276aa)


