---
title: CA2232:Windows フォームのエントリ ポイントを STAThread に設定します
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- MarkWindowsFormsEntryPointsWithStaThread
- CA2232
helpviewer_keywords:
- CA2232
- MarkWindowsFormsEntryPointsWithStaThread
ms.assetid: a3c95130-8e7f-4419-9fcd-b67d077e8efb
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 1bea8ee43c90c0e6559846bad00b61ec434ec46f
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/08/2019
ms.locfileid: "55923461"
---
# <a name="ca2232-mark-windows-forms-entry-points-with-stathread"></a>CA2232:Windows フォームのエントリ ポイントを STAThread に設定します

|||
|-|-|
|TypeName|MarkWindowsFormsEntryPointsWithStaThread|
|CheckId|CA2232|
|カテゴリ|Microsoft.Usage|
|互換性に影響する変更点|中断なし|

## <a name="cause"></a>原因
 アセンブリ参照、<xref:System.Windows.Forms>名前空間、およびそのエントリ ポイントでマークされていない、<xref:System.STAThreadAttribute?displayProperty=fullName>属性。

## <a name="rule-description"></a>規則の説明
 <xref:System.STAThreadAttribute> COM アプリケーションのモデルのスレッドがシングル スレッド アパートメントであることを示します。 この属性は、Windows フォームを使用するすべてのアプリケーションのエントリ ポイントに指定する必要があります。省略すると、Windows コンポーネントが正常に機能しないことがあります。 属性が存在しない場合、アプリケーションは、Windows フォームのサポートされていないマルチ スレッド アパートメント モデルを使用します。

> [!NOTE]
> [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] アプリケーション フレームワークを使用するプロジェクトをマークする必要はありません、 **Main**メソッドを stathread に設定します。 [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]コンパイラが自動的にことができます。

## <a name="how-to-fix-violations"></a>違反の修正方法
 このルールの違反を修正するには、追加、<xref:System.STAThreadAttribute>エントリ ポイントに属性します。 場合、<xref:System.MTAThreadAttribute?displayProperty=fullName>属性が存在する、それを削除します。

## <a name="when-to-suppress-warnings"></a>警告を抑制します。
 .NET Compact framework 開発している場合、この規則による警告を抑制するのには安全では、<xref:System.STAThreadAttribute>属性は不要であり、サポートされていません。

## <a name="example"></a>例
 次の例では、正しい使用法<xref:System.STAThreadAttribute>:

 [!code-csharp[FxCop.Usage.StaThread#1](../code-quality/codesnippet/CSharp/ca2232-mark-windows-forms-entry-points-with-stathread_1.cs)]
 [!code-vb[FxCop.Usage.StaThread#1](../code-quality/codesnippet/VisualBasic/ca2232-mark-windows-forms-entry-points-with-stathread_1.vb)]