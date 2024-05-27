# Сегментация медицинских снимков
Я решала задачу сегментации медицинских снимков: фото меланом и родинок. Датасет - [ADDI project](https://www.fc.up.pt/addi/ph2%20database.html).
<p align="center">
<img src="https://github.com/neirosetochka/medical_segmentation/assets/72963340/99cde7a0-203c-4637-b42f-37f1ab084f4e" height=70%>
</p>
Для этого по официальным статьям из архива были с нуля написаны SegNet и UNet:
<p float="left">
  <img src="https://github.com/neirosetochka/medical_segmentation/assets/72963340/e6398325-b817-4fdd-858d-d0514e681afd" width=40% />
  <img src="https://github.com/neirosetochka/medical_segmentation/assets/72963340/15ce45f2-cab3-44d1-971f-03cc173f2fb9" width=40% /> 
</p>
Метрика - IoU. Функций обучения было несколько:
$$\mathcal L_{BCE} = ^{y} - y^{y} + \log\left(1+\exp(-^{y})\right)$$
$$\mathcal L_{focal}(y, ^{y}) = -\sum_i \left[\left(1-\sigma(^{y}_i)\right)^\gamma y_i\log\sigma(^{y}_i) + (1-y_i)\log(1-\sigma(^{y}_i))\right]$$
