# MetaTRAN
A Lightweight Arbitrary-Scale Super-Resolution Reconstruction Method for Remote Sensing Images and a Real Satellite Dataset

## Our Code and Dataset will be released after publishing

Our code is built on [Meta-SR(PyTorch)].
## Attention

## Requirements


 
## train 
```
cd /Meta-SR-Pytorch 
python main.py --model metardn --save metardn --ext sep --lr_decay 200 --epochs 1000 --n_GPUs 2 --batch_size 16 
python main.py --model metaran --save metaran --ext sep --lr_decay 200 --epochs 1000 --n_GPUs 2 --batch_size 16 
python main.py --model metardan --save metardan --ext sep --lr_decay 200 --epochs 1000 --n_GPUs 2 --batch_size 16 
python main.py --model metatran --save metatran --ext sep --lr_decay 200 --epochs 1000 --n_GPUs 2 --batch_size 16 
python main.py --model metaran --save metaran --pre_train ./experiment/metaran/model/model_115.pt --resume 115 --lr 2.00e-5 --ext sep --lr_decay 200 --epochs 1000 --n_GPUs 2 --batch_size 16 
```
## test 
```
python main.py --model metardn --save metardn_Maocao_512 --ext sep --pre_train ./experiment/metardn/model/model_best.pt --test_only --data_test Macao_512  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results
python main.py --model metardn --save metardn_Maocao_512_last --ext sep --pre_train ./experiment/metardn/model/model_last.pt --test_only --data_test Macao_512  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results --sliding_window
python main.py --model metardn --save metardn_UCMerced_last --ext sep --pre_train ./experiment/metardn/model/model_last.pt --test_only --data_test UCMerced  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results --sliding_window
python main.py --model metardn --save metardn_AID_last --ext sep --pre_train ./experiment/metardn/model/model_last.pt --test_only --data_test AID  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results --sliding_window

python main.py --model metaran --save metaran_Maocao_512 --ext sep --pre_train ./experiment/metaran/model/model_best.pt --test_only --data_test Macao_512  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results
python main.py --model metaran --save metaran_Maocao_512_last --ext sep --pre_train ./experiment/metaran/model/model_last.pt --test_only --data_test Macao_512  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results --sliding_window
python main.py --model metaran --save metaran_UCMerced_last --ext sep --pre_train ./experiment/metaran/model/model_last.pt --test_only --data_test UCMerced  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results --sliding_window
python main.py --model metaran --save metaran_AID_last --ext sep --pre_train ./experiment/metaran/model/model_last.pt --test_only --data_test AID  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results --sliding_window

python main.py --model metardan --save metardan_Maocao_512 --ext sep --pre_train ./experiment/metardan/model/model_best.pt --test_only --data_test Macao_512  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results
python main.py --model metardan --save metardan_Maocao_512_last --ext sep --pre_train ./experiment/metardan/model/model_last.pt --test_only --data_test Macao_512  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results --sliding_window
python main.py --model metardan --save metardan_UCMerced_last --ext sep --pre_train ./experiment/metardan/model/model_last.pt --test_only --data_test UCMerced  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results --sliding_window
python main.py --model metardan --save metardan_AID_last --ext sep --pre_train ./experiment/metardan/model/model_last.pt --test_only --data_test AID  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results --sliding_window

python main.py --model metatran --save metatran_Maocao_512 --ext sep --pre_train ./experiment/metatran/model/model_best.pt --test_only --data_test Macao_512  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results --sliding_window
python main.py --model metatran --save metatran_Maocao_512_last --ext sep --pre_train ./experiment/metatran/model/model_last.pt --test_only --data_test Macao_512  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results --sliding_window
python main.py --model metatran --save metatran_UCMerced_last --ext sep --pre_train ./experiment/metatran/model/model_last.pt --test_only --data_test UCMerced  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results --sliding_window
python main.py --model metatran --save metatran_AID_last --ext sep --pre_train ./experiment/metatran/model/model_last.pt --test_only --data_test AID  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results --sliding_window

python main.py --model metardn --save metardn_Maocao_256 --ext sep --pre_train ./experiment/metardn/model/model_best.pt --test_only --data_test Macao_256  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results --no_eval
python main.py --model metaran --save metaran_Maocao_256 --ext sep --pre_train ./experiment/metaran/model/model_best.pt --test_only --data_test Macao_256  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results --no_eval
python main.py --model metardan --save metardan_Maocao_256 --ext sep --pre_train ./experiment/metardan/model/model_best.pt --test_only --data_test Macao_256  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results --no_eval
python main.py --model metatran --save metatran_Maocao_256 --ext sep --pre_train ./experiment/metatran/model/model_best.pt --test_only --data_test Macao_256  --scale 1.1+1.2+1.3+1.4+1.5+1.6+1.7+1.8+1.9+2.0+2.1+2.2+2.3+2.4+2.5+2.6+2.7+2.8+2.9+3.0+3.1+3.2+3.3+3.4+3.5+3.6+3.7+3.8+3.9+4.0+4.1+4.2+4.3+4.4+4.5+4.6+4.7+4.8+4.9+5.0+5.1+5.2+5.3+5.4+5.5+5.6+5.7+5.8+5.9+6.0+6.1+6.2+6.3+6.4+6.5+6.6+6.7+6.8+6.9+7.0+7.1+7.2+7.3+7.4+7.5+7.6+7.7+7.8+7.9+8.0 --n_GPUs 2 --save_results --no_eval --sliding_window
```
# Citation
```

```
# Contact
Xiaoyuan Wei (shiaoyuan@buaa.edu.cn)
