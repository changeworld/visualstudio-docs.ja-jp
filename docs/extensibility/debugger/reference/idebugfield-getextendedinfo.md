---
title: IDebugField::GetExtendedInfo |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugField::GetExtendedInfo
helpviewer_keywords:
- IDebugField::GetExtendedInfo method
ms.assetid: 46c0dd4d-4fd5-4efd-a908-71e4248e8e8d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0321dfbdc719d8e155bb1ee035032e2862bb90e0
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56679048"
---
# <a name="idebugfieldgetextendedinfo"></a>IDebugField::GetExtendedInfo
このメソッドは、フィールドに関する情報を拡張を取得します。

## <a name="syntax"></a>構文

```cpp
HRESULT GetExtendedInfo( 
   REFGUID guidExtendedInfo,
   BYTE**  prgBuffer,
   DWORD*  pdwLen
);
```

```csharp
int GetExtendedInfo(
   ref Guid guidExtendedInfo,
   IntPtr[] prgBuffer,
   ref uint pdwLen
);
```

#### <a name="parameters"></a>パラメーター
 `guidExtendedInfo`

 [in]返される情報を選択します。 次の値を指定できます。

|[値]|説明|
|-----------|-----------------|
|`guidConstantValue`|バイトのシーケンスとしての値。|
|`guidConstantType`|型の型シグネチャ。|

 `prgBuffer`

 [out]拡張情報を返します。

 `pdwLen`

 [入力、出力]拡張された情報のサイズをバイト単位で返します。

## <a name="return-value"></a>戻り値
 成功した場合、返します`S_OK`、それ以外のエラー コードを返します。

## <a name="remarks"></a>Remarks
 現時点では、このメソッドは、型または定数の値を返します。 呼び出し元で返されるバッファーを解放する必要があります`prgBuffer`呼び出して COM の`CoTaskMemFree`関数 (C++) または<xref:System.Runtime.InteropServices.Marshal.FreeCoTaskMem%2A>(c#)。

## <a name="see-also"></a>関連項目
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)