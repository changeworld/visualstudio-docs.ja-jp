---
title: IDebugFunctionObject::CreateObjectNoConstructor |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugFunctionObject::CreateObjectNoConstructor
helpviewer_keywords:
- IDebugFunctionObject::CreateObjectNoConstructor method
ms.assetid: 4e2bd6d5-f4bd-4c10-a998-3db451c9a0c8
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6a5ecd42b0ddf0138e98e2159fae1236ca02b473
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56707394"
---
# <a name="idebugfunctionobjectcreateobjectnoconstructor"></a>IDebugFunctionObject::CreateObjectNoConstructor
なしのコンス トラクターを持つオブジェクトを作成します。

## <a name="syntax"></a>構文

```cpp
HRESULT CreateObjectNoConstructor( 
   IDebugField*   pClassObject,
   IDebugObject** ppObject
);
```

```csharp
int CreateObjectNoConstructor(
   IDebugField      pClassField,
   out IDebugObject ppObject
);
```

#### <a name="parameters"></a>パラメーター
 `pClassObject`

 [in][IDebugField](../../../extensibility/debugger/reference/idebugfield.md)作成されるオブジェクトの型を表すオブジェクト。

 `ppObject`

 [out]返します、 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)新しく作成されたオブジェクトを表します。

## <a name="return-value"></a>戻り値
 成功した場合、S_OK を返します。それ以外の場合、エラー コードを返します。

## <a name="remarks"></a>Remarks
 ある複合型 (つまり、コンス トラクターは必要ありません)、関数のパラメーターによって表される、構造体のインスタンスを表すオブジェクトを作成するには、このメソッドを呼び出す、 [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)インターフェイス。

 オブジェクトのパラメーターは、コンス トラクターを必要とする場合、 [CreateObject](../../../extensibility/debugger/reference/idebugfunctionobject-createobject.md)メソッド。

## <a name="see-also"></a>関連項目
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
- [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)
- [CreateObject](../../../extensibility/debugger/reference/idebugfunctionobject-createobject.md)