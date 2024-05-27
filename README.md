# Сегментация медицинских снимков
Я решала задачу сегментации медицинских снимков: фото меланом и родинок. Датасет - [ADDI project](https://www.fc.up.pt/addi/ph2%20database.html).
<p align="center">
<img src="https://github.com/neirosetochka/medical_segmentation/assets/72963340/99cde7a0-203c-4637-b42f-37f1ab084f4e" width=80%>
</p>
Для этого по официальным статьям из архива были с нуля написаны SegNet и UNet:
<p float="left"> 
<img scr="https://github.com/neirosetochka/medical_segmentation/assets/72963340/5d229213-41b1-4ad3-86e3-b11808bc82c5" width=90%/> 
</p>
Метрика - IoU. Функций обучения было несколько:
$$\mathcal L_{BCE} = ^{y} - y^{y} + \log\left(1+\exp(-^{y})\right)$$
$$\mathcal L_{focal}(y, ^{y}) = -\sum_i \left[\left(1-\sigma(^{y}_i)\right)^\gamma y_i\log\sigma(^{y}_i) + (1-y_i)\log(1-\sigma(^{y}_i))\right]$$
