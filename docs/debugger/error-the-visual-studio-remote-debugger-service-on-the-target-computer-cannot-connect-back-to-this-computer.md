---
title: 'エラー: ターゲット コンピューター上の Visual Studio リモート デバッガーが、このコンピューターに接続できません'
titleSuffix: ''
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.service_access_denied_oncallback
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 823e4517deda68fc807c83373d26fc38740383c2
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MTE95
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "56713881"
---
# <a name="error-the-visual-studio-remote-debugger-service-on-the-target-computer-cannot-connect-back-to-this-computer"></a>エラー: ターゲット コンピューター上の Visual Studio リモート デバッガーが、このコンピューターに接続できません
このエラーは、Visual Studio リモート デバッガー サービスがデバッグを開始したコンピューターに接続するときに、このサービスを実行しているユーザー アカウントを認証できないことを示します。

 コンピューターにアクセスできるアカウントは、次の表のとおりです。

|||||
|-|-|-|-|
||LocalSystem アカウント|ドメイン アカウント|両方のコンピューターに同じユーザー名とパスワードを持つローカル アカウント|
|両方のコンピューターが同じドメインにある場合|はい|はい|はい|
|両方のコンピューターが双方向の信頼関係を持つドメインにある場合|いいえ|×|はい|
|一方または両方のコンピューターがワークグループにある場合|いいえ|×|はい|
|コンピューターが異なるドメインにある場合|いいえ|×|はい|

 さらに:

-   Visual Studio リモート デバッガー サービスを実行するアカウントは、すべてのプロセスをデバッグできるように、リモート コンピューターの管理者アカウントであることが必要です。

-   このアカウントには、**ローカル セキュリティ ポリシー**管理ツールを使用して、リモート コンピューターに対する `Log on as a service` 特権が与えられている必要もあります。

-   ローカル アカウントを使用してコンピューターにアクセスしている場合は、ローカル アカウントで Visual Studio リモート デバッガー サービスを実行する必要があります。

### <a name="to-correct-this-error"></a>このエラーを解決するには

1.  リモート コンピューターに Visual Studio リモート デバッガー サービスが正しく設定されていることを確認します。 詳細については、次を参照してください。[リモート デバッグ](../debugger/remote-debugging.md)します。

2.  上の表に示した、デバッガー ホスト コンピューターにアクセスできる適切なアカウントを使用して、リモート デバッガー サービスを実行します。

### <a name="to-add-log-on-as-a-service-privilege"></a>"サービスとしてログオンする" 特権を追加するには

1.  **[スタート]** メニューの **[コントロール パネル]** を選択します。

2.  必要に応じて、[コントロール パネル] で **[クラシック表示]** を選択します。

3.  **[管理ツール]** をダブルクリックします。 

4.  [管理ツール] ウィンドウで、**[ローカル セキュリティ ポリシー]** をダブルクリックします。

5.  **[ローカル セキュリティ設定]** ウィンドウで、**[ローカル ポリシー]** フォルダーを展開します。

6.  **[ユーザー権利の割り当て]** をクリックします。

7.  **[ポリシー]** 列の **[サービスとしてログオン]** をダブルクリックすると、現在のローカル グループ ポリシーの割り当てが **[サービスとしてログオン]** ダイアログ ボックスに表示されます。

8.  新しいユーザーを追加するには、**[ユーザーまたはグループの追加]** をクリックします。

9. ユーザーの追加作業が終了したら、**[OK]** をクリックします。

### <a name="to-work-around-this-error"></a>このエラーを回避するには

-   リモート デバッグ モニターをサービスとして実行する代わりに、アプリケーションとして実行します。

## <a name="see-also"></a>関連項目
- [リモート デバッグ エラーとトラブルシューティング](../debugger/remote-debugging-errors-and-troubleshooting.md)
- [Remote Debugging](../debugger/remote-debugging.md)