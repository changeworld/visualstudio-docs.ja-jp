---
title: IDebugObject::GetSize |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject::GetSize
helpviewer_keywords:
- IDebugObject::GetSize method
ms.assetid: 89af423b-36eb-479d-b2de-2693455eca15
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a44f7c20784ca7f253db1d44c4079603f363d616
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56719731"
---
# <a name="idebugobjectgetsize"></a>IDebugObject::GetSize
オブジェクトのサイズをバイト単位で取得します。

## <a name="syntax"></a>構文

```cpp
HRESULT GetSize( 
   UINT* pnSize
);
```

```csharp
int GetSize(
   out uint pnSize
);
```

#### <a name="parameters"></a>パラメーター
 `pnSize`

 [out]サイズをバイト単位で返します。

## <a name="return-value"></a>戻り値
 成功した場合、S_OK を返します。それ以外の場合、エラー コードを返します。

## <a name="remarks"></a>Remarks
 使用して、 [GetValue](../../../extensibility/debugger/reference/idebugobject-getvalue.md)バイトのシーケンスとして値を取得するメソッド。

## <a name="see-also"></a>関連項目
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)
- [GetValue](../../../extensibility/debugger/reference/idebugobject-getvalue.md)