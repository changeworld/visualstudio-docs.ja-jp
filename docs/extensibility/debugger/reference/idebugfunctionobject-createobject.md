---
title: IDebugFunctionObject::CreateObject |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugFunctionObject::CreateObject
helpviewer_keywords:
- IDebugFunctionObject::CreateObject method
ms.assetid: c4c99dd5-609a-4e7c-8f29-eb728f57e995
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 54d1e6c21cdf4e16db69cbad0947e864e7c1847e
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56689929"
---
# <a name="idebugfunctionobjectcreateobject"></a>IDebugFunctionObject::CreateObject
コンス トラクターを使用してオブジェクトを作成します。

## <a name="syntax"></a>構文

```cpp
HRESULT CreateObject( 
   IDebugFunctionObject* pConstructor,
   DWORD                 dwArgs,
   IDebugObject*         pArgs[],
   IDebugObject**        ppObject
);
```

```csharp
int CreateObject(
   IDebugFunctionObject pConstructor,
   uint                 dwArgs,
   IDebugObject[]       pArgs,
   out IDebugObject     ppObject
);
```

#### <a name="parameters"></a>パラメーター
 `pConstructor`

 [in][IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)を作成するオブジェクトのコンス トラクターを表すオブジェクト。

 `dwArgs`

 [in]パラメーターの数、`pArg`配列。 コンス トラクターに渡されるパラメーターの数を表します。

 `pArg`

 [in]配列の[IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)コンス トラクターに渡されるパラメーターを表すオブジェクトします。

 `ppObject`

 [out]返します、`IDebugObject`新しく作成されたオブジェクトを表します。

## <a name="return-value"></a>戻り値
 成功した場合、S_OK を返します。それ以外の場合、エラー コードを返します。

## <a name="remarks"></a>Remarks
 クラス (またはその他の複合型コンス トラクターが必要です) のインスタンスを表すオブジェクトを作成するには、このメソッドを呼び出すによって表される関数のパラメーターは、 [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)インターフェイス。

 オブジェクトのパラメーターにコンス トラクターを必要としない場合、 [CreateObjectNoConstructor](../../../extensibility/debugger/reference/idebugfunctionobject-createobjectnoconstructor.md)メソッド。

## <a name="see-also"></a>関連項目
- [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)
- [CreateObjectNoConstructor](../../../extensibility/debugger/reference/idebugfunctionobject-createobjectnoconstructor.md)