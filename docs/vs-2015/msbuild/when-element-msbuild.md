---
title: When 要素 (MSBuild) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#When
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- <When> Element [MSBuild]
- When Element [MSBuild]
ms.assetid: eb27de6f-4e71-4e87-87e2-d93f7bf5899c
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 93fd259e00d7a8f849b97cb97c3f950cd95f57ed
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/19/2019
ms.locfileid: "54761543"
---
# <a name="when-element-msbuild"></a>When 要素 (MSBuild)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
`Choose` 要素で選ぶ対象のコード ブロックを指定します。  
  
 \<Project>  
 \<Choose>  
 \<When>  
 \<Choose>  
 ...  
 \<Otherwise>  
 \<Choose>  
 ...  
  
## <a name="syntax"></a>構文  
  
```  
<When Condition="'StringA'=='StringB'">  
    <PropertyGroup>... </PropertyGroup>  
    <ItemGroup>... </ItemGroup>  
    <Choose>... </Choose>  
</When>  
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
  
|属性|説明|  
|---------------|-----------------|  
|条件|必須の属性です。<br /><br /> 評価する条件です。 詳細については、「[条件](../msbuild/msbuild-conditions.md)」を参照してください。|  
  
### <a name="child-elements"></a>子要素  
  
|要素|説明|  
|-------------|-----------------|  
|[Choose](../msbuild/choose-element-msbuild.md)|省略可能な要素です。<br /><br /> 子要素を評価して、実行するコードのセクションを 1 つ選びます。 `Choose` 要素に 0 個以上の `When` 要素があります。|  
|[ItemGroup](../msbuild/itemgroup-element-msbuild.md)|省略可能な要素です。<br /><br /> ユーザー定義 [Item](../msbuild/item-element-msbuild.md) 要素のセットが含まれます。 `ItemGroup` 要素に 0 個以上の `When` 要素があります。|  
|[PropertyGroup](../msbuild/propertygroup-element-msbuild.md)|省略可能な要素です。<br /><br /> ユーザー定義の [Property](../msbuild/property-element-msbuild.md) 要素のセットを格納します。 `PropertyGroup` 要素に 0 個以上の `When` 要素があります。|  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|[Choose 要素 (MSBuild)](../msbuild/choose-element-msbuild.md)|子要素を評価して、実行するコードのセクションを 1 つ選びます。|  
  
## <a name="remarks"></a>解説  
 `Condition` 属性が true と評価された場合、その `When` 要素の子の `ItemGroup` 要素と `PropertyGroup` 要素が実行されて、後続の `When` 要素はすべてスキップされます。  
  
 `Choose`、`When`、`Otherwise` 要素を組み合わせて使って、実行される可能性のある複数のコード セクションから 1 つを選びます。 詳細については、「[条件構造](../msbuild/msbuild-conditional-constructs.md)」を参照してください。  
  
## <a name="example"></a>例  
 次のプロジェクトでは、`Choose` 要素を使って、設定する `When` 要素のプロパティ値のセットを選んでいます。 両方の `When` 要素の `Condition` 属性が `false` と評価された場合、`Otherwise` 要素のプロパティ値が設定されます。  
  
```  
<Project  
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003" >  
    <PropertyGroup>  
        <Configuration Condition="'$(Configuration)' == ''">Debug</Configuration>  
        <OutputType>Exe</OutputType>  
        <RootNamespace>ConsoleApplication1</RootNamespace>  
        <AssemblyName>ConsoleApplication1</AssemblyName>  
        <WarningLevel>4</WarningLevel>  
    </PropertyGroup>  
    <Choose>  
        <When Condition=" '$(Configuration)'=='debug' ">  
            <PropertyGroup>  
                <DebugSymbols>true</DebugSymbols>  
                <DebugType>full</DebugType>  
                <Optimize>false</Optimize>  
                <OutputPath>.\bin\Debug\</OutputPath>  
                <DefineConstants>DEBUG;TRACE</DefineConstants>  
            </PropertyGroup>  
            <ItemGroup>  
                <Compile Include="UnitTesting\*.cs" />  
                <Reference Include="NUnit.dll" />  
            </ItemGroup>  
        </When>  
        <When Condition=" '$(Configuration)'=='retail' ">  
            <PropertyGroup>  
                <DebugSymbols>false</DebugSymbols>  
                <Optimize>true</Optimize>  
                <OutputPath>.\bin\Release\</OutputPath>  
                <DefineConstants>TRACE</DefineConstants>  
            </PropertyGroup>  
        </When>  
        <Otherwise>  
            <PropertyGroup>  
                <DebugSymbols>true</DebugSymbols>  
                <Optimize>false</Optimize>  
                <OutputPath>.\bin\$(Configuration)\</OutputPath>  
                <DefineConstants>DEBUG;TRACE</DefineConstants>  
            </PropertyGroup>  
        </Otherwise>  
    </Choose>  
    <Import Project="$(MSBuildBinPath)\Microsoft.CSharp.targets" />  
</Project>  
```  
  
## <a name="see-also"></a>関連項目  
 [条件構造](../msbuild/msbuild-conditional-constructs.md)   
 [プロジェクト ファイル スキーマ リファレンス](../msbuild/msbuild-project-file-schema-reference.md)
