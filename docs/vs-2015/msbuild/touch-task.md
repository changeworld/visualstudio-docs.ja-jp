---
title: Touch タスク | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#Touch
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, Touch task
- Touch task [MSBuild]
ms.assetid: 8a978645-1393-4904-ae69-42afabd8c109
caps.latest.revision: 20
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: eb0ab3daf6d23d9a70a9889479bdf6a19ddec041
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/19/2019
ms.locfileid: "54762557"
---
# <a name="touch-task"></a>Touch タスク
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
ファイルのアクセス時刻および変更時刻を設定します。  
  
## <a name="parameters"></a>パラメーター  
 `Touch` タスクのパラメーターの説明を次の表に示します。  
  
|パラメーター|説明|  
|---------------|-----------------|  
|`AlwaysCreate`|省略可能な `Boolean` 型のパラメーターです。<br /><br /> `true` の場合、まだ存在しないファイルが作成されます。|  
|`Files`|必須の <xref:Microsoft.Build.Framework.ITaskItem>`[]` 型のパラメーターです。<br /><br /> タッチするファイルのコレクションを指定します。|  
|`ForceTouch`|省略可能な `Boolean` 型のパラメーターです。<br /><br /> `true` の場合、ファイルが読み取り専用でもファイルにタッチします。|  
|`Time`|省略可能な `String` 型のパラメーターです。<br /><br /> 現在の時刻以外の時刻を指定します。 <xref:System.DateTime.Parse%2A> メソッドで有効な形式で指定する必要があります。|  
|`TouchedFiles`|省略可能な <xref:Microsoft.Build.Framework.ITaskItem>`[]` 型の出力パラメーターです。<br /><br /> 正常にタッチされた項目のコレクションが含まれます。|  
  
## <a name="remarks"></a>解説  
 上記のパラメーター以外に、このタスクは <xref:Microsoft.Build.Tasks.TaskExtension> クラスからパラメーターを継承します。このクラス自体は、<xref:Microsoft.Build.Utilities.Task> クラスから継承されます。 これらの追加のパラメーターの一覧とその説明については、「 [TaskExtension Base Class](../msbuild/taskextension-base-class.md)」を参照してください。  
  
## <a name="example"></a>例  
 次の例では `Touch` タスクを使用して、`Files` 項目コレクションに指定されたファイルのアクセス時刻および更新時刻を変更し、`FilesTouched` 項目コレクションに正常にタッチされたファイルのリストを配置しています。  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  
<ItemGroup>  
    <Files Include="File1.cs;File2.cs;File3.cs" />  
</ItemGroup>  
  
    <Target Name="TouchFiles">  
        <Touch  
            Files="@(Files)">  
            <Output  
                TaskParameter="TouchedFiles"  
                ItemName="FilesTouched"/>  
    </Touch>  
</Target>  
</Project>  
```  
  
## <a name="see-also"></a>関連項目  
 [タスク](../msbuild/msbuild-tasks.md)   
 [Task Reference (タスク リファレンス)](../msbuild/msbuild-task-reference.md)
