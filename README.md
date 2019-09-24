# FairNAS: Rethinking Evaluation Fairness of Weight Sharing Neural Architecture Search


## Introduction

we propose a novel idea called Fair Neural Architecture Search (FairNAS), in which a strict fairness constraint is enforced for fair inheritance and training. In this way, our supernet exhibits nice convergence and very high training accuracy. The performance of any sampled model loaded with shared weights from the supernet strongly correlates with that of stand-alone counterpart when trained fully. This result dramatically improves the searching efficiency, with a multi-objective reinforced evolutionary search backend, our pipeline generated a new set of state-of-the-art architectures on ImageNet: FairNAS-A attains 75.34% top-1 validation accuracy on ImageNet, FairNAS-B 75.10%, FairNAS-C 74.69%, even with lower multi-adds and/or fewer number of parameters compared with others.

The architectures of FairNAS-A,B,C are drawn below. 

![](images/fairnas-architectures.png)

## Requirements
* Python 3.6 +
* Pytorch 1.0.1 +

## Discuss with us!

* QQ 群名称：小米 AutoML 交流反馈
* 群   号：702473319 (加群请填写“神经网络架构搜索”的英文简称)

## Good news! We Are Hiring (Full-time & Internship)!

Hi folks! We are AutoML Team from Xiaomi AI Lab, based in Beijing, China. There are few open positions, welcome applications from new graduates and professionals skilled in Deep Learning (Vision, Speech, NLP etc.)!

* Please send your resume to `zhangbo11@xiaomi.com`
* 人工智能算法/软件工程师（含实习生）职位，简历请发送至 `zhangbo11@xiaomi.com`

## Updates
* Jul-3-2019： Model release of FairNAS-A, FairNAS-B, FairNAS-C.

## Performance Result
![](images/result.png)

## Preprocessing
We have reorganized all validation images of the ILSVRC2012 ImageNet by their classes.

1. Download ILSVRC2012 ImageNet dataset.

2. Change to ILSVRC2012 directory and run the preprocessing script with
    ```
     ./preprocess_val_dataset.sh
    ```

## Evaluate

To evaluate,
    
    python3 verify.py --model [FairNAS_A|FairNAS_B|FairNAS_C] --device [cuda|cpu] --val-dataset-root [ILSVRC2012 root path] --pretrained-path [pretrained model path]
    

## Citation

Your kind citations are welcomed!

    @article{chu2019fairnas,
        title={FairNAS: Rethinking Evaluation Fairness of Weight Sharing Neural Architecture Search},
        author={Chu, Xiangxiang and Zhang, Bo and Xu, Ruijun and Li, Jixiang},
        journal={arXiv preprint arXiv:1907.01845},
        url={https://arxiv.org/pdf/1907.01845.pdf},
        year={2019}
    }
