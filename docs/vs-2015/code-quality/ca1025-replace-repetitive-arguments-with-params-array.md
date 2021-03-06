---
title: 'Ca 1025: を params 配列で反復する引数を置き換える |Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- CA1025
- ReplaceRepetitiveArgumentsWithParamsArray
helpviewer_keywords:
- ReplaceRepetitiveArgumentsWithParamsArray
- CA1025
ms.assetid: f009b340-dea3-4459-8fe1-2143aa8b5d0b
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: b649a5eaa26365fcf7b620ae10db037269716b08
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/23/2018
ms.locfileid: "49912813"
---
# <a name="ca1025-replace-repetitive-arguments-with-params-array"></a>CA1025: 反復する引数を params 配列で置き換えます
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|ReplaceRepetitiveArgumentsWithParamsArray|
|CheckId|CA1025|
|カテゴリ|Microsoft.Design|
|互換性に影響する変更点|なし|

## <a name="cause"></a>原因
 パブリック型の public または protected のメソッドが複数の 3 つのパラメーターとその最後の 3 つのパラメーターは、同じ型。

## <a name="rule-description"></a>規則の説明
 引数の正確な数は不明であり、可変個引数は同じ型、または同じの型として渡すことができる場合、引数を繰り返すのではなく、パラメーター配列を使用します。 たとえば、<xref:System.Console.WriteLine%2A>メソッドは、パラメーター配列を使用して、任意の数をそのまま使用する汎用のオーバー ロードを提供します。<xref:System.Object>引数。

## <a name="how-to-fix-violations"></a>違反の修正方法
 この規則違反を修正するには、パラメーター配列で引数を繰り返すを置き換えます。

## <a name="when-to-suppress-warnings"></a>警告を抑制する状況
 この規則による警告を抑制しても安全では常にただし、この設計では、ユーザビリティの問題を生じる可能性があります。

## <a name="example"></a>例
 次の例では、この規則に違反する型を示します。

 [!code-csharp[FxCop.Design.RepeatArgs#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.RepeatArgs/cs/FxCop.Design.RepeatArgs.cs#1)]



