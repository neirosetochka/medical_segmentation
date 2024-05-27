# Сегментация медицинских снимков
Я решала задачу сегментации мединских снимков: фото меланом и родинок. Датасет - [ссылка](https://www.fc.up.pt/addi/ph2%20database.html).
<p align="center">
<img src="https://github.com/neirosetochka/medical_segmentation/assets/72963340/3b4fe19f-0c63-42bc-930d-ffe46ca765e2"> 
</p>
Для этого по официальным статьям из архива были с нуля написаны SegNet и UNet:
<p float="left">
  <img src="https://github.com/neirosetochka/medical_segmentation/assets/72963340/e6398325-b817-4fdd-858d-d0514e681afd" />
  <img src="https://github.com/neirosetochka/medical_segmentation/assets/72963340/15ce45f2-cab3-44d1-971f-03cc173f2fb9" /> 
</p>
Метрика - IoU. Функций обучения было несколько:
$$\mathcal L_{BCE} = \hat y - y\hat y + \log\left(1+\exp(-\hat y)\right)$$
$$\mathcal L_{focal}(y, \hat y) = -\sum_i \left[\left(1-\sigma(\hat y_i)\right)^\gamma y_i\log\sigma(\hat y_i) + (1-y_i)\log(1-\sigma(\hat y_i))\right]$$
