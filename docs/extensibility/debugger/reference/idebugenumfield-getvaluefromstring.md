---
title: IDebugEnumField::GetValueFromString |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEnumField::GetValueFromString
helpviewer_keywords:
- IDebugEnumField::GetValueFromString method
ms.assetid: 1ef8ac5e-a3e0-4078-b876-7f5615aedcbb
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e714e6b2028605eb9c820f904cedf9ed4c23eab8
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56716026"
---
# <a name="idebugenumfieldgetvaluefromstring"></a>IDebugEnumField::GetValueFromString
このメソッドは、列挙定数の名前に関連付けられている値を返します。

## <a name="syntax"></a>構文

```cpp
HRESULT GetValueFromString(
   LPCOLESTR  pszValue,
   ULONGLONG* pvalue
);
```

```csharp
int GetValueFromString(
   string    pszValue,
   out ulong pValue
);
```

#### <a name="parameters"></a>パラメーター
 `pszValue`

 [in]値を取得する対象の名前を指定する文字列。 C++、ワイド文字の文字列は、このことに注意してください。

 `pValue`

 [out]関連付けられている数値を返します。

## <a name="return-value"></a>戻り値
 成功した場合、返します`S_OK`。 それ以外を返します`S_FALSE`名前列挙型、またはエラー コードの一部でない場合は、します。

## <a name="remarks"></a>Remarks
 このメソッドは大文字小文字を区別します。 (たとえば、名前は大文字小文字を区別しない、Visual Basic などの言語) で、大文字と小文字が必要に応じて、使用して[GetValueFromStringCaseInsensitive](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstringcaseinsensitive.md)します。

## <a name="see-also"></a>関連項目
- [IDebugEnumField](../../../extensibility/debugger/reference/idebugenumfield.md)
- [GetValueFromStringCaseInsensitive](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstringcaseinsensitive.md)