# Azure Kinect DKの使い方
基本的にazure kinect dkの[公式ドキュメント](https://docs.microsoft.com/ja-jp/azure/Kinect-dk/)を参考にする

[SDKのgithubレポジトリ](https://github.com/microsoft/Azure-Kinect-Sensor-SDK)


## Azure Kinect Sensor SDKのダウンロード(Linux)
1. [リポジトリの接続](https://docs.microsoft.com/ja-jp/windows-server/administration/linux-package-repository-for-microsoft-software) →これでaptでインストール可能になる
2. `sudo apt install k4a-tools`
3. インストール時のツールのバージョンを確認  
![tool install terminal](../images/Screenshot_terminal.png
)  
→画像だとバージョンが1.4だとわかる
4. チュートリアルで使用するパッケージ `sudo apt install libk4a<バージョン>-dev`  
→バージョンが違うとインストール時にエラーがでるので注意

# Azure Kinect Viewrの起動
ダウンロードを行った環境で`k4aviewer`を実行することで起動する

# Azure Kinect をROSで使用する
[AzureKinectDK ROSドライバのレポジトリ](https://github.com/microsoft/Azure_Kinect_ROS_Driver)

`roslaunch azure_kinect_ros_driver driver.launch`  
を実行することでドライバが起動する

rvizにてpointCloud2を追加し, Topicを設定することでデータを確認できる

## 