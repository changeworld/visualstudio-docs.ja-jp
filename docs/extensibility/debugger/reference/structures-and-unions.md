---
title: 構造体と共用体 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- structures [Visual Studio SDK]
ms.assetid: 9ff0a8f8-1ee6-4fdd-8b80-206436ff589b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e0ef171d24b3744657a2cb05338b2b124a6331c9
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56692529"
---
# <a name="structures-and-unions"></a>構造体と共用体
構造体と共用体では、Visual Studio Debugging SDK を次に示します。

- [AD_PROCESS_ID](../../../extensibility/debugger/reference/ad-process-id.md)システム ID または GUID 可能性のあるプロセス ID を指定します。

- [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md)ブレークポイントが発生する条件について説明します。

- [BP_ERROR_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-error-resolution-info.md)場所、プログラム、およびスレッドなど、エラー ブレークポイントの解決方法について説明します。

- [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md)ブレークポイントの位置を記述するために使用する構造体の型を指定します。

- [BP_LOCATION_CODE_ADDRESS](../../../extensibility/debugger/reference/bp-location-code-address.md)コード内のアドレスのブレークポイントの場所を記述するコンポーネントを定義します。

- [BP_LOCATION_CODE_CONTEXT](../../../extensibility/debugger/reference/bp-location-code-context.md)デバッグ中のプログラム内のアドレスに直接バインドされているブレークポイントの場所について説明します。

- [BP_LOCATION_CODE_FILE_LINE](../../../extensibility/debugger/reference/bp-location-code-file-line.md)コード ソース ファイル内の行のブレークポイントの場所について説明します。

- [BP_LOCATION_CODE_FUNC_OFFSET](../../../extensibility/debugger/reference/bp-location-code-func-offset.md)コード内の関数のブレークポイントのオフセット位置を示します。

- [BP_LOCATION_CODE_STRING](../../../extensibility/debugger/reference/bp-location-code-string.md) IDE から、ユーザーは入力文字列に基づくコードのブレークポイントを設定するために使用します。

- [BP_LOCATION_DATA_STRING](../../../extensibility/debugger/reference/bp-location-data-string.md)ユーザーは、IDE から入力を文字列に基づくデータ ブレークポイントを設定するために使用します。

- [BP_LOCATION_RESOLUTION](../../../extensibility/debugger/reference/bp-location-resolution.md)特定の位置にブレークポイントの解決方法について説明します。

- [BP_PASSCOUNT](../../../extensibility/debugger/reference/bp-passcount.md)以前通過した後に発生するブレークポイントとなる、カウントと条件について説明します。

- [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md)ブレークポイントを実装するために必要な情報が含まれています。

- [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md)ブレークポイントを実装するために必要な情報が含まれています (と同じ、 [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md)構造体には、仕入先の GUID、制約、およびトレース ポイントの情報が含まれています)。

- [BP_RESOLUTION_CODE](../../../extensibility/debugger/reference/bp-resolution-code.md)コードのブレークポイントの場所について説明します。

- [BP_RESOLUTION_DATA](../../../extensibility/debugger/reference/bp-resolution-data.md)データ ブレークポイントのバインドの結果について説明します。

- [BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md)コードのブレークポイントまたは データ ブレークポイントのバインドされたブレークポイント情報について説明します。

- [BP_RESOLUTION_LOCATION](../../../extensibility/debugger/reference/bp-resolution-location.md)ブレークポイント解像度の位置の構造を指定します。

- [BSTR_ARRAY](../../../extensibility/debugger/reference/bstr-array.md)文字列の配列について説明します。

- [BUILT_TYPE](../../../extensibility/debugger/reference/built-type.md)メタデータから取得したフィールドの種類に関する情報を指定します。

- [CODE_PATH](../../../extensibility/debugger/reference/code-path.md)関数またはメソッドの呼び出しについて説明します。

- [COMPUTER_INFO](../../../extensibility/debugger/reference/computer-info.md)デバッガーが実行されているコンピューターについて説明します。

- [CONST_GUID_ARRAY](../../../extensibility/debugger/reference/const-guid-array.md) Guid のリストについて説明します。

- [CONTEXT_INFO](../../../extensibility/debugger/reference/context-info.md)メモリ コンテキストまたはコードのコンテキストについて説明します。

- [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md)デバッグ中のプログラムでは、住所をについて説明します。

- [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md)アドレスのさまざまな種類の数値の 1 つを表します。

- [DEBUG_CUSTOM_VIEWER](../../../extensibility/debugger/reference/debug-custom-viewer.md)識別カスタム ビューアーまたは型のビジュアライザーです。

- [DEBUG_PROPERTY_INFO](../../../extensibility/debugger/reference/debug-property-info.md)を名前、種類、および値を持つ階層的な性質のオブジェクトをさらに説明するデバッグのプロパティについて説明します。

- [DEBUG_REFERENCE_INFO](../../../extensibility/debugger/reference/debug-reference-info.md)参照を記述します。

- [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md)逆アセンブリには、IDE の表示について説明します。

- [EXCEPTION_INFO](../../../extensibility/debugger/reference/exception-info.md)デバッグ中のプログラムによってスローされた例外、実行時エラーを説明します。

- [FIELD_INFO](../../../extensibility/debugger/reference/field-info.md)ローカル変数、パラメーター、またはその他のフィールドについて説明します。

- [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md)スタック フレームをについて説明します。

- [GUID_ARRAY](../../../extensibility/debugger/reference/guid-array.md)使用可能なデバッグ エンジンの一意の識別子の配列について説明します。

- [JMC_CODE_SPEC](../../../extensibility/debugger/reference/jmc-code-spec.md)モジュールの JustMyCode 情報を設定するために使用します。

- [MACHINE_INFO](../../../extensibility/debugger/reference/machine-info.md)特定のコンピューターについて説明します。

- [METADATA_ADDRESS_ARRAYELEM](../../../extensibility/debugger/reference/metadata-address-arrayelem.md)配列内の配列要素について説明します。

- [METADATA_ADDRESS_FIELD](../../../extensibility/debugger/reference/metadata-address-field.md)クラスまたは構造体のフィールドのアドレスについて説明します。

- [METADATA_ADDRESS_LOCAL](../../../extensibility/debugger/reference/metadata-address-local.md) (通常関数またはメソッド) のスコープ内でローカル変数のアドレスについて説明します。

- [METADATA_ADDRESS_METHOD](../../../extensibility/debugger/reference/metadata-address-method.md)クラスのメソッドのアドレスについて説明します。

- [METADATA_ADDRESS_PARAM](../../../extensibility/debugger/reference/metadata-address-param.md)メソッドまたは関数のパラメーターについて説明します。

- [METADATA_ADDRESS_RETVAL](../../../extensibility/debugger/reference/metadata-address-retval.md)メソッドまたは関数からの戻り値について説明します。

- [METADATA_TYPE](../../../extensibility/debugger/reference/metadata-type.md)メタデータから取得したフィールドの種類について説明します。

- [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md)特定のモジュール (DLL、exe ファイルまたはアセンブリ) について説明します。

- [MODULE_SYMBOL_SEARCH_INFO](../../../extensibility/debugger/reference/module-symbol-search-info.md)シンボル検索パスが検索されをに関する状態情報について説明します。

- [NATIVE_ADDRESS](../../../extensibility/debugger/reference/native-address.md)ネイティブのアドレスについて説明します。

- [PDB_TYPE](../../../extensibility/debugger/reference/pdb-type.md) PDB シンボルから取得したフィールドの種類について説明します。

- [PENDING_BP_STATE_INFO](../../../extensibility/debugger/reference/pending-bp-state-info.md)コードの場所にバインドする準備が整っているブレークポイントの状態について説明します。

- [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md)プロセスについて説明します。

- [PROGRAM_NODE_ARRAY](../../../extensibility/debugger/reference/program-node-array.md)の一覧をについて説明します。 [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)プログラム ノードを表すオブジェクト。

- [PROVIDER_PROCESS_DATA](../../../extensibility/debugger/reference/provider-process-data.md)マシンで実行中のプロセスについて説明します。

- [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md)指定されたテキストの行と列の場所について説明します。

- [THREADPROPERTIES](../../../extensibility/debugger/reference/threadproperties.md)スレッドのプロパティについて説明します。

- [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md)フィールドの型について説明します。

- [UNMANAGED_ADDRESS_PHYSICAL](../../../extensibility/debugger/reference/unmanaged-address-physical.md)物理アドレスについて説明します。

- [UNMANAGED_ADDRESS_THIS_RELATIVE](../../../extensibility/debugger/reference/unmanaged-address-this-relative.md)が関連しているアドレスについて説明します、`this`ポインター (`Me` Visual Basic で)。

## <a name="requirements"></a>必要条件
 ヘッダー: msdbg.h、sh.h、または ee.h

 名前空間: Microsoft.VisualStudio.Debugger.Interop

 アセンブリ:Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>関連項目
- [API リファレンス](../../../extensibility/debugger/reference/api-reference-visual-studio-debugging.md)