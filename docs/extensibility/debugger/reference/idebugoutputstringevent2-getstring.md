---
title: IDebugOutputStringEvent2::GetString |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugOutputStringEvent2::GetString
helpviewer_keywords:
- IDebugOutputStringEvent2::GetString
ms.assetid: f059f8e0-ad44-49ac-ba90-73576ada5e06
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d310df2e30a0c6e2b59bb561c2cfdcb8a7ac6254
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56718210"
---
# <a name="idebugoutputstringevent2getstring"></a>IDebugOutputStringEvent2::GetString
表示可能なメッセージを取得します。

## <a name="syntax"></a>構文

```cpp
HRESULT GetString( 
   BSTR* pbstrString
);
```

```csharp
int GetString( 
   out string pbstrString
);
```

#### <a name="parameters"></a>パラメーター
 `pbstrString`

 [out]表示可能なメッセージが返されます。

## <a name="return-value"></a>戻り値
 成功した場合、返します`S_OK`、それ以外のエラー コードを返します。

## <a name="see-also"></a>関連項目
- [IDebugOutputStringEvent2](../../../extensibility/debugger/reference/idebugoutputstringevent2.md)