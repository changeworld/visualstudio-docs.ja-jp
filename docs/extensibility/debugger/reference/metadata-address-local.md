---
title: METADATA_ADDRESS_LOCAL |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- METADATA_ADDRESS_LOCAL
helpviewer_keywords:
- METADATA_ADDRESS_LOCAL structure
ms.assetid: 635f6bc5-c486-4e0e-83db-36f15e543843
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2f8366b8a18c2512aa55f2bab70ac9523e9265f5
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56700303"
---
# <a name="metadataaddresslocal"></a>METADATA_ADDRESS_LOCAL

この構造体は、(通常関数またはメソッド) のスコープ内でローカル変数のアドレスを表します。

## <a name="syntax"></a>構文

```cpp
typedef struct _tagMETADATA_ADDRESS_LOCAL {
    _mdToken  tokMethod;
    IUnknown* pLocal;
    DWORD     dwIndex;
} METADATA_ADDRESS_LOCAL;
```

```csharp
public struct METADATA_ADDRESS_LOCAL {
    public int    tokMethod;
    public object pLocal;
    public uint   dwIndex;
}
```

## <a name="terms"></a>用語

`tokMethod`

メソッドまたは関数の ID、ローカル変数は一部です。

[C++]`_mdToken`は、 `typedef` 32 ビット`int`します。

`pLocal`

この構造体を表すアドレスを持つトークン。

`dwIndex`

このローカル変数、メソッドまたは関数、またはその他の値 (言語固有) でのインデックスを指定できます。

## <a name="remarks"></a>Remarks

この構造体の共用体の一部は、 [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md)ときに構造体、`dwKind`のフィールド、`DEBUG_ADDRESS_UNION`構造に設定されている`ADDRESS_KIND_LOCAL`(からの値、 [ADDRESS_KIND](../../../extensibility/debugger/reference/address-kind.md)列挙型)。

> [!WARNING]
> [C++ のみ]場合`pLocal`を呼び出す必要がありますが null でない`Release`、トークンのポインター (`addr`内のフィールドには、 [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md)構造)。
>
> ```cpp
> if (addr.dwKind == ADDRESS_KIND_METADATA_LOCAL && addr.addr.addrLocal.pLocal != NULL)
> {
     addr.addr.addrLocal.pLocal->Release();
> }
> ```

## <a name="requirements"></a>必要条件

ヘッダー: sh.h

名前空間: Microsoft.VisualStudio.Debugger.Interop

アセンブリ:Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>関連項目

- [構造体と共用体](../../../extensibility/debugger/reference/structures-and-unions.md)
- [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md)
- [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md)
- [ADDRESS_KIND](../../../extensibility/debugger/reference/address-kind.md)
