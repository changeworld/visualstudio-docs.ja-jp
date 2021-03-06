---
title: CA1013:オーバーロードする加算および減算で、演算子 equals をオーバーロードします
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- OverrideOperatorEqualsOnOverridingAddAndSubtract
- OverrideOperatorEqualsOnOverloadingAddAndSubtract
- CA1013
- OverloadOperatorEqualsOnOverloadingAddAndSubtract
helpviewer_keywords:
- OverrideOperatorEqualsOnOverloadingAddAndSubtract
- OverrideOperatorEqualsOnOverridingAddAndSubtract
- CA1013
- OverloadOperatorEqualsOnOverloadingAddAndSubtract
ms.assetid: 5bd28d68-c179-49ff-af47-5250b8b18a10
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 76a3790f57882071bddc90ef78a0ac74dd565514
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/08/2019
ms.locfileid: "55915905"
---
# <a name="ca1013-overload-operator-equals-on-overloading-add-and-subtract"></a>CA1013:オーバーロードする加算および減算で、演算子 equals をオーバーロードします

|||
|-|-|
|TypeName|OverloadOperatorEqualsOnOverloadingAddAndSubtract|
|CheckId|CA1013|
|カテゴリ|Microsoft.Design|
|互換性に影響する変更点|なし|

## <a name="cause"></a>原因
 パブリック型またはプロテクト型で、等値演算子を実装しないまま、加算演算子または減算演算子を実装しています。

## <a name="rule-description"></a>規則の説明
 返すには、等しいかどうかを定義する型のインスタンスは、加算や減算などの操作を使用して組み合わせることができます、ほぼ常にする必要があります`true`同じの構成値を持つ 2 つのインスタンス。

 オーバー ロードされた等値演算子の実装では、既定の等値演算子を使用できません。 こうと、スタック オーバーフローが発生します。 等値演算子を実装するには、実装で、Object.Equals メソッドを使用します。 次の例を参照してください。

```vb
If (Object.ReferenceEquals(left, Nothing)) Then
    Return Object.ReferenceEquals(right, Nothing)
Else
    Return left.Equals(right)
End If
```

```csharp
if (Object.ReferenceEquals(left, null))
    return Object.ReferenceEquals(right, null);
return left.Equals(right);
```

## <a name="how-to-fix-violations"></a>違反の修正方法
 この規則違反を修正するには、加算と減算演算子と数学的に矛盾があるように、等値演算子を実装します。

## <a name="when-to-suppress-warnings"></a>警告を抑制します。
 等値演算子の既定の実装の種類の正しい動作を提供するときに、この規則による警告を非表示にも安全です。

## <a name="example"></a>例
 次の例では、型を定義する (`BadAddableType`) をこの規則に違反します。 この型は、テスト、同じフィールド値を持つ 2 つのインスタンスに等値演算子を実装する必要があります`true`等しいかどうか。 型`GoodAddableType`修正の実装を示しています。 この型も非等値演算子を実装し、上書きことに注意してください<xref:System.Object.Equals%2A>を他のルールを満たすためにします。 完全な実装は実装も<xref:System.Object.GetHashCode%2A>します。

 [!code-csharp[FxCop.Design.AddAndSubtract#1](../code-quality/codesnippet/CSharp/ca1013-overload-operator-equals-on-overloading-add-and-subtract_1.cs)]

## <a name="example"></a>例
 次の例は、等値演算子の既定値と正しい動作を説明するためには、このトピックで以前に定義された型のインスタンスを使用して、等しいかどうかテストします。

 [!code-csharp[FxCop.Design.TestAddAndSubtract#1](../code-quality/codesnippet/CSharp/ca1013-overload-operator-equals-on-overloading-add-and-subtract_2.cs)]

この例を実行すると、次の出力が生成されます。

```txt
Bad type:  {2,2} {2,2} are equal? No
Good type: {3,3} {3,3} are equal? Yes
Good type: {3,3} {3,3} are == ?   Yes
Bad type:  {2,2} {9,9} are equal? No
Good type: {3,3} {9,9} are == ?   No
```

## <a name="see-also"></a>関連項目

- [等値演算子](/dotnet/standard/design-guidelines/equality-operators)