---
title: AsyncTaskMethodBuilder&lt;TResult&gt;構造体の内部メンバー |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- AsyncTaskMethodBuilder<TResult> structure [.NET Framework debug engines]
- debug engines, AsyncTaskMethodBuilder<TResult> structure [.NET Framework]
ms.assetid: 17ebc340-8170-4aff-bf54-dc4548c83632
caps.latest.revision: 5
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 966a6ee224ac14707ed411e7e63c9473831c7003
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2018
ms.locfileid: "51792347"
---
# <a name="asynctaskmethodbuilderlttresultgt-structure---internal-members"></a>AsyncTaskMethodBuilder&lt;TResult&gt;構造体の内部メンバー
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

このトピックでの内部メンバーの説明、<xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder%601>クラス。 このクラスの詳細については、次を参照してください。、<xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder%601>リファレンス トピック。  
  
 **名前空間:** <xref:System.Runtime.CompilerServices?displayProperty=fullName>  
  
 **アセンブリ:** mscorlib (mscorlib.dll 内)  
  
 .NET Framework からこれらの内部メンバーにアクセスできないため、次の構文には共通中間言語 (CIL) が提供されます。  
  
## <a name="syntax"></a>構文  
  
```  
.class public sequential ansi sealed beforefieldinit System.Runtime.CompilerServices.AsyncTaskMethodBuilder`1<TResult>  
       extends System.ValueType  
       implements System.Runtime.CompilerServices.IAsyncMethodBuilder  
```  
  
## <a name="internal-members"></a>内部メンバー  
  
|名前|説明|  
|----------|-----------------|  
|[ObjectIdForDebugger プロパティ](../../extensibility/debugger/asynctaskmethodbuilder-tresult-objectidfordebugger-property.md)|デバッガーには、このビルダーを一意に識別するために使用するオブジェクトを取得します。|  
|[m_task フィールド](../../extensibility/debugger/asynctaskmethodbuilder-tresult-m-task-field.md)|遅延初期化タスクの構築を表します。|  
  
## <a name="see-also"></a>関連項目  
 <xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder%601>   
 [.NET Framework の並列拡張機能の内部](../../extensibility/debugger/parallel-extension-internals-for-the-dotnet-framework.md)

