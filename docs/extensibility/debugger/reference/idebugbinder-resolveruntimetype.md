---
title: IDebugBinder::ResolveRuntimeType |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugBinder::ResolveRuntimeType
helpviewer_keywords:
- IDebugBinder::ResolveRuntimeType method
ms.assetid: 6456ab3e-1c03-4f3c-91f9-16797ab7f5e7
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: f1d4622e1de76406568cda4761005c5482f3169d
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56699198"
---
# <a name="idebugbinderresolveruntimetype"></a>IDebugBinder::ResolveRuntimeType
このメソッドは、オブジェクトの実行時の型を決定します。

## <a name="syntax"></a>構文

```cpp
HRESULT ResolveRuntimeType( 
   IDebugObject* pObject,
   IDebugField** ppResolved
);
```

```csharp
int ResolveRuntimeType(
   IDebugObject     pObject,
   out IDebugField  ppResolved
);
```

#### <a name="parameters"></a>パラメーター
 `pObject`

 [in][IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)を解決できます。

 `ppResolved`

 [out]オブジェクトの型を返します、 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)します。

## <a name="return-value"></a>戻り値
 成功した場合、返します`S_OK`、それ以外のエラー コードを返します。

## <a name="remarks"></a>Remarks
 オブジェクトの実行時の型はコンパイル時に常には認識されません。 たとえば、ポリモーフィズムを使用して、引数ことができます関数として渡すボタン クラスなど、基本クラス。 実際の引数は、ラジオ ボタン クラスなどの派生クラスで可能性があります。

## <a name="see-also"></a>関連項目
- [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md)
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)