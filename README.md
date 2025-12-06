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

## 参考にした
[PINTO model zooの歩き方 ~ Tour of PINTO model zoo ~](https://zenn.dev/karaage0703/articles/a4973dc094ee1c)


## 何がある？
###  Image Classification

### 2D Object Detection

### 3D Object Detection
### 2D/3D Face Detection
### 2D/3D Hand Detection
### 2D/3D Human/Animal Pose Estimation
### Depth Estimation from Monocular/Stereo Images
### Semantic Segmentation
### Anomaly Detection
### Artistic
### Super Resolution
### Sound Classifier
### Natural Language Processing
### Text Recognition
### Action Recognition
### Inpainting
### GAN
### Transformer
### Others


## ROS2で使う
### EdgeYOLO-ROS
[EdgeYOLO-ROS](https://github.com/fateshelled/EdgeYOLO-ROS)は、モデルを PINTO_model_zoo からダウンロードして使う前提 で作られた ROS2 パッケージです。



#### weights
[356_EdgeYOLO](https://github.com/PINTO0309/PINTO_model_zoo/tree/main/356_EdgeYOLO)から一括ダウンロードできます。




### YOLOX-ROS
[YOLOX-ROS](https://github.com/Ar-Ray-code/YOLOX-ROS)はROS2 + ONNX(cuDNN) /TFLite/ TensorRT でアンカーフリーな物体検出をするためのパッケージで、PINTO_model_zoo 由来の YOLOX モデルを流用しやすい。

[Ar-Ray-code/YOLOX-ROS](https://github.com/Ar-Ray-code/YOLOX-ROS)さんのAr-Ray-code/YOLOX-ROS:humbleをフォークして修正しました。

[YOLOX-ROS](https://github.com/okadahiroyuki/YOLOX-ROS.git)をご覧ください。

[Dockerで動かす](https://github.com/okadahiroyuki/YOLOX-ROS/tree/humble/yolox_ros_cpp/docker/onnxruntime)のが楽だと思います。

#### weights
ONNXモデルは[YOLOX公式リポジトリ](https://github.com/Megvii-BaseDetection/YOLOX/tree/main/demo/ONNXRuntime) で公開されています。

- YOLOX-Nano	0.91M	1.08	416x416	25.8	[github](https://github.com/Megvii-BaseDetection/YOLOX/tree/main/demo/ONNXRuntime#:~:text=25.8-,github,-YOLOX%2DTiny)
- YOLOX-Tiny	5.06M	6.45	416x416	32.8	[github](https://github.com/Megvii-BaseDetection/YOLOX/releases/download/0.1.1rc0/yolox_tiny.onnx)
- YOLOX-S	9.0M	26.8	640x640	40.5	[github](https://github.com/Megvii-BaseDetection/YOLOX/releases/download/0.1.1rc0/yolox_s.onnx)
- YOLOX-M	25.3M	73.8	640x640	47.2	[github](https://github.com/Megvii-BaseDetection/YOLOX/tree/main/demo/ONNXRuntime#:~:text=47.2-,github,-YOLOX%2DL)
- YOLOX-L	54.2M	155.6	640x640	50.1	[github](https://github.com/Megvii-BaseDetection/YOLOX/releases/download/0.1.1rc0/yolox_l.onnx)
- YOLOX-Darknet53	63.72M	185.3	640x640	48.0	[github](https://github.com/Megvii-BaseDetection/YOLOX/tree/main/demo/ONNXRuntime#:~:text=48.0-,github,-YOLOX%2DX)
- YOLOX-X	99.1M	281.9	640x640	51.5	[github](https://github.com/Megvii-BaseDetection/YOLOX/releases/download/0.1.1rc0/yolox_x.onnx)
```
./src/YOLOX-ROS/weights/onnx/download.bash all
```
で一括ダウンロードできます。





