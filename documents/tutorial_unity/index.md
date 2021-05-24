# Unity上でリギング済みOpen DiaperをHumanoidに装着する

## 概要

本手順書では、Boothにて配布中の着せ替え支援ボーン移植エディタを利用して、Unity上でリギング済みOpen DiaperをHumanoid 3Dモデルに装着する手順を説明します。


[着せ替え支援ボーン移植エディタ](https://booth.pm/ja/items/954433)

## 準備

下記のソフトウェアをインストールしておきます。

- Unity 2018.4.20f1（2021年5月現在のVRChat SDK対応バージョン）
- 着せ替え支援ボーン移植エディタ
- Open DiaperのUnitypackage、プロジェクト内の「SetupForUnity/OpenDiaperV2ForUnity.unitypackage」に存在
- Open Diaperを装着する対象のHumanoid 3Dモデル


## 作業手順

1. Unity上で新しいシーンを作成する
![Unity上で新しいシーンを作成する](image/2021-05-24-19-33-24.png)
![新しいシーンを開く](image/2021-05-24-22-44-50.png)

1. ヒエラルキーにHumanoid 3Dモデルをドラッグアンドドロップする
![ヒエラルキーにHumanoid 3Dモデルをドラッグアンドドロップする](image/2021-05-24-22-46-45.png)

1. ヒエラルキーにOpen Diaper 3Dモデルをドラッグアンドドロップする
![ヒエラルキーにOpen Diaper 3Dモデルをドラッグアンドドロップする](image/2021-05-24-22-48-34.png)

1. Humanoid 3Dモデルを右クリックして、「Unpack prefab」を実行する
![Humanoid 3Dモデルを右クリックして、「Unpack prefab」を実行する](image/2021-05-24-22-48-58.png)

1. Open Diaper 3Dモデルを右クリックして、「Unpack prefab」を実行する
![Open Diaper 3Dモデルを右クリックして、「Unpack prefab」を実行する](image/2021-05-24-22-50-17.png)

1. メニューバーの「Cloth Editor」→「Bone setup」から着せ替え支援ボーン移植エディタを開く
![メニューバーの「Cloth Editor」→「Bone setup」から着せ替え支援ボーン移植エディタを開く](image/2021-05-24-22-55-24.png)
着せ替え支援ボーン移植エディタを開いたところ
![着せ替え支援ボーン移植エディタを開いたところ](image/2021-05-24-22-55-51.png)

1. Cloth objの欄に、Open Diaperオブジェクトを設定する
![Cloth objの欄に、Open Diaperオブジェクトを設定する](image/2021-05-24-23-03-13.png)

1. Model objの欄に、Humanoid 3Dモデルオブジェクトを設定する
![Model objの欄に、Humanoid 3Dモデルオブジェクトを設定する](image/2021-05-24-23-03-36.png)

1. 右側のLoadボタンをクリックし、SetupForUnity/opendiaper_kisekae.xmlを読み込む
![右側のLoadボタンをクリックし、SetupForUnity/opendiaper_kisekae.xmlを読み込む](image/2021-05-24-23-00-08.png)
opendiaper_kisekae.xml読み込み完了後
![opendiaper_kisekae.xml読み込み完了後](image/2021-05-24-23-00-34.png)

1. Humanoid 3Dモデルの対象ボーンを着せ替え支援ボーン移植エディタに設定する
![Humanoid 3Dモデルの対象ボーンを着せ替え支援ボーン移植エディタに設定する](image/2021-05-24-23-01-44.png)
対象となるボーンは、上からHips、Spine、UpperLeg_L、UpperLeg_Rです。

1. Open Diaperオブジェクトの位置とサイズを合わせる
![Open Diaperオブジェクトの位置とサイズを合わせる](image/2021-05-24-23-05-54.png)

1. 「Bone Parent Setup」ボタンを押して着せ替えを実行する
![「Bone Parent Setup」ボタンを押して着せ替えを実行する](image/2021-05-24-23-06-32.png)
ダイアログボックスを読み、OKボタンをクリックする
![ダイアログボックスを読み、OKボタンをクリックする](image/2021-05-24-23-06-54.png)

1. Humanoid 3Dモデルと親子関係になるように、Open Diaper 3DモデルをHumanoid 3Dモデルにドラッグアンドドロップする
![Humanoid 3Dモデルと親子関係になるように、Open Diaper 3DモデルをHumanoid 3Dモデルにドラッグアンドドロップする](image/2021-05-24-23-07-58.png)

1. Humanoid 3Dモデルの脚を動かして、Open Diaperがボーンに追従するかを確かめる
![Humanoid 3Dモデルの脚を動かして、Open Diaperがボーンに追従するかを確かめる](image/2021-05-24-23-08-33.png)
確認したら、元に戻しておく
![確認したら、元に戻しておく](image/2021-05-24-23-09-06.png)

以上の手順で完了となります。

この後、VRChatにアップロードする場合には、通常のVRChat SDKを用いたアバターの設定が必要となります。
