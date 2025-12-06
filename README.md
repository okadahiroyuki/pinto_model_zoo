# PINTO_model_zooを使う

PINTO0309 氏が管理している “model zoo”（モデル集）で、様々な機械学習モデルを 複数のフレームワーク・フォーマット間で変換済み の状態で提供しています。 

対応しているフォーマット/フレームワークには、以下のようなものがあります。 
- TensorFlow
- PyTorch
- ONNX
- OpenVINO
- TensorFlow.js (TFJS)
- TensorRT (TF-TRT)
- TensorFlow Lite（Float32／Float16／INT8）
- EdgeTPU
- CoreML

## 特長・メリット
- マルチフレームワーク・フォーマット：多くのフォーマット間で変換済みモデルが揃っており、例えば “PyTorchからONNX→TensorFlow Lite” という変換を自分でやる必要が少ない。

- 量子化モデル（INT8／Float16）にも対応：軽量化／高速化・組み込み用途で有用な量子化済みモデルも多数。 

- 実習・プロトタイピングの時間短縮：例えば教育用途（あなたのように大学で機械学習・AIを教えている方）だと、「すぐ動かせるモデル」があることで講義／演習設計がラクになります。


## ROS2で使う
### EdgeYOLO-ROS
[EdgeYOLO-ROS](https://github.com/fateshelled/EdgeYOLO-ROS)は、モデルを PINTO_model_zoo からダウンロードして使う前提 で作られた ROS2 パッケージです。



### YOLOX-ROS
[YOLOX-ROS](https://github.com/Ar-Ray-code/YOLOX-ROS)はROS2 + ONNX(cuDNN) /TFLite/ TensorRT でアンカーフリーな物体検出をするためのパッケージで、PINTO_model_zoo 由来の YOLOX モデルを流用しやすい。

[Ar-Ray-code/YOLOX-ROS](https://github.com/Ar-Ray-code/YOLOX-ROS)さんのAr-Ray-code/YOLOX-ROS:humbleをフォークして修正しました。

[YOLOX-ROS](https://github.com/okadahiroyuki/YOLOX-ROS.git)をご覧ください。

[Dockerで動かす](https://github.com/okadahiroyuki/YOLOX-ROS/tree/humble/yolox_ros_cpp/docker/onnxruntime)のが楽だと思います。







