---
title: IDebugProgram2::GetENCUpdate |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgram2::GetENCUpdate
helpviewer_keywords:
- IDebugProgram2::GetENCUpdate
ms.assetid: 9832aac8-6320-4fd8-91dd-2a0852febb00
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 485684486c8d58dc9c7cbd3e679138360d02fdbb
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56708317"
---
# <a name="idebugprogram2getencupdate"></a>IDebugProgram2::GetENCUpdate
このメソッドは、このプログラムの編集と続行 (ENC) の更新プログラムを取得します。 カスタム デバッグ エンジンは常に返します`E_NOTIMPL`します。

## <a name="syntax"></a>構文

```cpp
HRESULT GetENCUpdate( 
   IUnknown** ppUpdate
);
```

```csharp
int GetENCUpdate(
   out object ppUpdate
);
```

#### <a name="parameters"></a>パラメーター
 `ppUpdate`

 [out]このプログラムを更新するために使用する内部インターフェイスを返します。

## <a name="return-value"></a>戻り値
 成功した場合、返します`S_OK`、それ以外のエラー コードを返します。

> [!NOTE]
>  カスタム デバッグ エンジンは常に返す必要があります`E_NOTIMPL`します。

## <a name="see-also"></a>関連項目
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)