---
title: IDebugBinder3::GetTypeArgumentCount |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugBinder3::GetTypeArgumentCount
helpviewer_keywords:
- IDebugBinder3::GetTypeArgumentCount method
ms.assetid: caf68de6-6f7c-4efd-b803-121347a5032e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 77d4140a37577fa5bf4734e386300e062ef80399
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56725048"
---
# <a name="idebugbinder3gettypeargumentcount"></a>IDebugBinder3::GetTypeArgumentCount
このメソッドは、このオブジェクトに関連付けられている引数の型の数を返します。

## <a name="syntax"></a>構文

```cpp
HRESULT GetTypeArgumentCount(
   UINT* uCount
);
```

```csharp
int GetTypeArgumentCount(
   out uint uCount
);
```

#### <a name="parameters"></a>パラメーター
 `uCount`

 [out]このオブジェクトに関連付けられている引数の型の数。

## <a name="return-value"></a>戻り値
 成功した場合、返します`S_OK`、それ以外のエラー コードを返します。

## <a name="remarks"></a>Remarks
 このメソッドによって返される値がで使用するための配列を割り当てることができます、 [GetTypeArguments](../../../extensibility/debugger/reference/idebugbinder3-gettypearguments.md)メソッド。

## <a name="see-also"></a>関連項目
- [IDebugBinder3](../../../extensibility/debugger/reference/idebugbinder3.md)
- [GetTypeArguments](../../../extensibility/debugger/reference/idebugbinder3-gettypearguments.md)