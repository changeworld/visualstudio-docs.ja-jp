---
title: '方法: プロジェクトに固有のエディターを開く |Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- project types, opening a project-specific editor
- editors [Visual Studio SDK], opening project-specific editors
- projects [Visual Studio SDK], opening folders
ms.assetid: 83e56d39-c97b-4c6b-86d6-3ffbec97e8d1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4d90a748627b3a2345e40eac7c1894e87673d1ca
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56693257"
---
# <a name="how-to-open-project-specific-editors"></a>方法: 開いているプロジェクト固有のエディター
プロジェクトで開かれている項目のファイルは本質的に、そのプロジェクトの特定のエディターにバインドする場合、プロジェクトは、プロジェクトに固有のエディターを使用してファイルを開く必要があります。 ファイルは、エディターを選択するため、IDE のメカニズムには委任できません。 たとえば、標準のビットマップ エディターを使用する代わりには、プロジェクトに一意のファイルの情報を認識する特定のビットマップ エディターを指定するのにこのプロジェクト固有のエディター オプションを使用できます。

 IDE の呼び出し、<xref:Microsoft.VisualStudio.Shell.Interop.IVsProject3.OpenItem%2A>メソッドによって、特定のプロジェクト ファイルを開く必要がありますかを決定します。 詳細については、次を参照してください。[ファイルを開くコマンドを使用してファイルを表示](../extensibility/internals/displaying-files-by-using-the-open-file-command.md)します。 次のガイドラインを使用して実装する、`OpenItem`メソッドに、プロジェクトをプロジェクトに固有のエディターを使用してファイルを開きます。

## <a name="to-implement-the-openitem-method-with-a-project-specific-editor"></a>プロジェクト固有のエディターで OpenItem メソッドを実装するには

1.  呼び出す、<xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocumentTable.FindAndLockDocument%2A>メソッド (`RDT_EditLock`) をファイル (ドキュメント データ オブジェクト) が既に開いているかどうかを判断します。

    > [!NOTE]
    >  ドキュメント データとドキュメント ビュー オブジェクトの詳細については、次を参照してください。[ドキュメント カスタム エディターでのデータとドキュメント ビュー](../extensibility/document-data-and-document-view-in-custom-editors.md)します。

2.  ファイルが既に開いている場合は、呼び出すことによって、ファイルを再び表面化、<xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument.IsDocumentOpen%2A>メソッドとの IDO_ActivateIfOpen の値を指定する、`grfIDO`パラメーター。

     ファイルが開かれていると、ドキュメントには、呼び出し元プロジェクト以外のプロジェクトが所有は、別のプロジェクトから開いているエディターであるユーザーに警告が表示されます。 [ファイル] ウィンドウに表示されるからです。

3.  テキスト バッファー (ドキュメント データ オブジェクト) が既に開いてに別のビューをアタッチする場合は、するはそのビューをフックする責任を負います。 プロジェクトから、表示 (ドキュメント ビュー オブジェクト) をインスタンス化するための推奨アプローチは次のとおりです。

    1.  呼び出す`QueryService`上、<xref:Microsoft.VisualStudio.Shell.Interop.SLocalRegistry>へのポインターを取得するサービス、<xref:Microsoft.VisualStudio.Shell.Interop.ILocalRegistry2>インターフェイス。

    2.  呼び出す、<xref:Microsoft.VisualStudio.Shell.Interop.ILocalRegistry2.CreateInstance%2A>ドキュメント ビュー クラスのインスタンスを作成するメソッド。

4.  呼び出す、<xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell.CreateDocumentWindow%2A>ドキュメント ビュー オブジェクトを指定するメソッド。

     このメソッドはサイト、ドキュメント ウィンドウにドキュメント ビュー オブジェクトです。

5.  実行するか、適切な呼び出し、<xref:Microsoft.VisualStudio.Shell.Interop.IPersistFileFormat.InitNew%2A>または<xref:Microsoft.VisualStudio.Shell.Interop.IPersistFileFormat.Load%2A>メソッド。

     この時点では、完全に初期化され、開くことができるビューがあります。

6.  呼び出す、<xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.Show%2A>メソッドを表示し、ビューを開きます。

## <a name="see-also"></a>関連項目
- [開き、プロジェクト項目の保存](../extensibility/internals/opening-and-saving-project-items.md)
- [方法: 標準のエディターを開く](../extensibility/how-to-open-standard-editors.md)
- [方法: 開いているドキュメントのエディターを開く](../extensibility/how-to-open-editors-for-open-documents.md)