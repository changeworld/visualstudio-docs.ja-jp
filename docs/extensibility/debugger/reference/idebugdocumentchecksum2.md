---
title: IDebugDocumentChecksum2 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugDocumentChecksum2 interface
ms.assetid: 6d22fa94-21aa-46cb-b5b5-32a6399ebb20
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9b40129cb8623e6ea68babe2c480da4e4d4198f3
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56685587"
---
# <a name="idebugdocumentchecksum2"></a>IDebugDocumentChecksum2
デバッグ ドキュメントのチェックサムを表し、コンポーネント間のチェックサムを渡すことができます。

## <a name="syntax"></a>構文

```
IDebugDocumentChecksum2 : IUnknown
```

## <a name="notes-for-implementers"></a>実装についてのメモ
 このインターフェイスを公開するすべてのコンポーネントで実装することができます、 [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)インターフェイス。 ただし、主により実装されますデバッグ エンジン シンボル ファイル (*.pdb) に埋め込まれているチェックサムは、IDE に戻されますしてソースを検索するときに使用できるようにします。

## <a name="methods"></a>メソッド
 次の表は、メソッドの`IDebugDocumentChecksum2`します。

|メソッド|説明|
|------------|-----------------|
|[GetChecksumAndAlgorithmId](../../../extensibility/debugger/reference/idebugdocumentchecksum2-getchecksumandalgorithmid.md)|使用するバイトの最大数を指定されたドキュメントのチェックサムとアルゴリズム識別子を取得します。|

## <a name="requirements"></a>必要条件
 ヘッダー:Msdbg.h

 名前空間: Microsoft.VisualStudio.Debugger.Interop

 アセンブリ:Microsoft.VisualStudio.Debugger.Interop.dll