---
title: Idialoadcallback::notifydebugdir |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- IDiaLoadCallback::NotifyDebugDir method
ms.assetid: bd04e2f6-0dbf-4742-a556-96f2cd99aa19
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 04a41e03a679a8910bb408162da57078e27eb654
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2018
ms.locfileid: "51769556"
---
# <a name="idialoadcallbacknotifydebugdir"></a>IDiaLoadCallback::NotifyDebugDir
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

.Exe ファイルでデバッグ ディレクトリが見つかったときに呼び出されます。  
  
## <a name="syntax"></a>構文  
  
```cpp#  
HRESULT NotifyDebugDir (   
   BOOL  fExecutable,  
   DWORD cbData,  
   BYTE  data[]  
);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `fExecutable`  
 [in]`TRUE` (.dbg ファイルではなく) 実行可能ファイルからデバッグ ディレクトリは読み取り専用である場合。  
  
 `cbData`  
 [in]デバッグ ディレクトリ内のデータのバイト数をカウントします。  
  
 `data[]`  
 [in]デバッグ ディレクトリに設定している配列。  
  
## <a name="return-value"></a>戻り値  
 成功した場合、返します`S_OK`、それ以外のエラー コードを返します。 リターン コードは通常は無視されます。  
  
## <a name="remarks"></a>Remarks  
 [Idiadatasource::loaddataforexe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)メソッドが実行可能ファイルの処理中にデバッグ ディレクトリを見つけたときに、このコールバックを呼び出します。  
  
 このメソッドは、.pdb ファイル内にある以外のデバッグ情報をサポートするためにリバース エンジニア リング、実行可能ファイルやデバッグ ファイルをクライアントの必要性を削除します。 このデータは、クライアントは、利用可能なデバッグ情報の種類と実行可能ファイルまたは .dbg ファイルに存在するかどうかを認識できます。  
  
 は、ほとんどのクライアントにこのコールバックは必要ありません、`IDiaDataSource::loadDataForExe`メソッドが透過的にシンボルを処理するために必要な場合に、.pdb と .dbg の両方のファイルを開きます。  
  
## <a name="see-also"></a>関連項目  
 [IDiaLoadCallback2](../../debugger/debug-interface-access/idialoadcallback2.md)   
 [IDiaDataSource::loadDataForExe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)



