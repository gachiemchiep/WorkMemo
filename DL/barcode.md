# Barcode detect, decode using DL

## Some good posts

[Decoding 1-D Barcode from Degraded Images Using a Neural Network](http://what-when-how.com/computer-visionimaging-and-computer-graphics/decoding-1-d-barcode-from-degraded-images-using-a-neural-network-computer-visionimaging-and-computer-graphics-part-1/)

[Paper here](https://pdfs.semanticscholar.org/5f5e/fa7cf8a821b8997a5ff641771d3030db2f78.pdf)

The existing open-source libraries for 1-D barcodes recognition are not able to recognize the codes 
from images acquired using simple devices without autofocus or macro function

ZXing project : best open-source barcode decoed, but still need need autofocus and high resolution

This papaer : use image restoration technique to improve accuracy of Barcode decoder

流れの概要

1. Image restoration
2. Barcodes Decoding
2.1 Identification
2.2 Decoding

They used very small network and added directly into ZXing library. 

[Reading barcodes with
neural networks](https://pdfs.semanticscholar.org/380a/e14aa6f260ee85cc062da6631e84d6ee68cd.pdf)

EAN-13 barcode（13桁だけ）だけ対応しています。

流れの概要

1. PyBarを用いて、Barcode画像生成する
2. 生成された画像をAugmenting techniqueで学習データ生成
3. CNNの出力は　１３x１０サイズのベクトルです。各ベクトル（size: 10）で
　　一つの桁の数値を読み出します。
  
 Poorly written thesis

