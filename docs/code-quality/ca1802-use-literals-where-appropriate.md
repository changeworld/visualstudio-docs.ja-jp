---
title: CA1802:適切な場所にリテラルを使用します
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- UseLiteralsWhereAppropriate
- CA1802
helpviewer_keywords:
- UseLiteralsWhereAppropriate
- CA1802
ms.assetid: 2515e4cd-9e61-486d-b067-58ba1a743ce4
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 4f6b469ccce9cc5297cf9c328b05822aef9e3e29
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/08/2019
ms.locfileid: "55925255"
---
# <a name="ca1802-use-literals-where-appropriate"></a>CA1802:適切な場所にリテラルを使用します

|||
|-|-|
|TypeName|UseLiteralsWhereAppropriate|
|CheckId|CA1802|
|カテゴリ|Microsoft.Performance|
|互換性に影響する変更点|なし|

## <a name="cause"></a>原因
 フィールドが宣言されている`static`と`readonly`(`Shared`と`ReadOnly`で[!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)])、およびコンパイル時に計算される値で初期化されます。

## <a name="rule-description"></a>規則の説明
 値を`static``readonly`フィールドは、宣言型の静的コンス トラクターが呼び出されたときに実行時に計算されます。 場合、`static``readonly`フィールドは宣言されているし、静的コンス トラクターが明示的に宣言しないコンパイラは、フィールドを初期化するために静的コンス トラクターを生成するときに初期化されます。

 値を`const`フィールドがコンパイル時に計算し、と比較した場合、実行時のパフォーマンスを向上すると、メタデータに格納されている、`static``readonly`フィールド。

 対象フィールドに割り当てられた値は、コンパイル時に計算、ために宣言を変更、`const`フィールド値は実行時ではなく、コンパイル時に計算されます。

## <a name="how-to-fix-violations"></a>違反の修正方法
 このルールの違反を修正するには、置換、`static`と`readonly`修飾子を`const`修飾子。

## <a name="when-to-suppress-warnings"></a>警告を抑制します。
 パフォーマンスが重大な問題がない場合、この規則による警告を抑制またはルールを無効にも安全です。

## <a name="example"></a>例
 次の例は、型`UseReadOnly`、ルールと、型に違反する`UseConstant`ルールを満たします。

 [!code-vb[FxCop.Performance.UseLiterals#1](../code-quality/codesnippet/VisualBasic/ca1802-use-literals-where-appropriate_1.vb)]
 [!code-csharp[FxCop.Performance.UseLiterals#1](../code-quality/codesnippet/CSharp/ca1802-use-literals-where-appropriate_1.cs)]