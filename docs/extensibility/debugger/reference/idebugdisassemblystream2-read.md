---
title: IDebugDisassemblyStream2::Read |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugDisassemblyStream2::Read
helpviewer_keywords:
- IDebugDisassemblyStream2::Read
ms.assetid: 7db5f6bb-73ee-45bc-b187-c1b6aa2dfdd5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: eb204ccb98d0c7f5a6f5eeac9ccbc5ea07dfae16
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56688460"
---
# <a name="idebugdisassemblystream2read"></a>IDebugDisassemblyStream2::Read
手順については、混合モードのストリームの現在位置から始まるを読み取ります。

## <a name="syntax"></a>構文

```cpp
HRESULT Read( 
   DWORD                     dwInstructions,
   DISASSEMBLY_STREAM_FIELDS dwFields,
   DWORD*                    pdwInstructionsRead,
   DisassemblyData*          prgDisassembly
);
```

```csharp
int Read( 
   uint                           dwInstructions,
   enum_DISASSEMBLY_STREAM_FIELDS dwFields,
   out uint                       pdwInstructionsRead,
   DisassemblyData[]              prgDisassembly
);
```

#### <a name="parameters"></a>パラメーター
 `dwInstructions`

 [in]逆アセンブルする命令の数。 この値はの最大長でも、`prgDisassembly`配列。

 `dwFields`

 [in]フラグの組み合わせ、 [DISASSEMBLY_STREAM_FIELDS](../../../extensibility/debugger/reference/disassembly-stream-fields.md)のどのフィールドを示す列挙`prgDisassembly`を記入します。

 `pdwInstructionsRead`

 [out]実際に逆アセンブルされた命令の数を返します。

 `prgDisassembly`

 [out]配列の[DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md)構造体を逆アセンブルしたコード、逆アセンブルした命令ごとに 1 つの構造が入力されます。 この配列の長さはによって異なります、`dwInstructions`パラメーター。

## <a name="return-value"></a>戻り値
 成功した場合、返します`S_OK`、それ以外のエラー コードを返します。

## <a name="remarks"></a>Remarks
 呼び出すことによって、現在のスコープで使用可能な命令の最大数を取得できます、 [GetSize](../../../extensibility/debugger/reference/idebugdisassemblystream2-getsize.md)メソッド。

 呼び出してから、次の命令は読み取り専用の現在の位置を変更できます、[シーク](../../../extensibility/debugger/reference/idebugdisassemblystream2-seek.md)メソッド。

 `DSF_OPERANDS_SYMBOLS`にフラグを追加することができます、`DSF_OPERANDS`フラグ、`dwFields`パラメーターを逆アセンブルするときにシンボル名を使用することを示します。

## <a name="see-also"></a>関連項目
- [IDebugDisassemblyStream2](../../../extensibility/debugger/reference/idebugdisassemblystream2.md)
- [DISASSEMBLY_STREAM_FIELDS](../../../extensibility/debugger/reference/disassembly-stream-fields.md)
- [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md)
- [GetSize](../../../extensibility/debugger/reference/idebugdisassemblystream2-getsize.md)
- [Seek](../../../extensibility/debugger/reference/idebugdisassemblystream2-seek.md)