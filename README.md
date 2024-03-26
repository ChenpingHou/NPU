# NPU
# # Code of NPU(**Confidence-based PU Learning with Instance-Dependent Label Noise**)

## Overview
This is the code for the paper "Confidence-based PU Learning with Instance-Dependent Label Noise", which proposes a novel method Noisy PU(NPU) for dealing PU learning under instance-dependent label noise problem. 

## Main Files
There are two main files to implement NPU method in the paper. 
* NPU_train.m: the main algorithm code.

  Syntax:
  > model = NPU_train(positive_data, confidence, unlabeled_data, pi0, alpha, lambda)
  
  Description:
  NPU_train takes:
  - positive_data - A Npxd array, the ith positive instance is stored in positive_data(i,:)
  - confidence - A 1xNp array, the confidence of ith positive instance is stored in confidence(1,i)
  - unlabeled_data - A Nuxd array, the jth unlabeled instance is stored in unlabeled_data(j,:)
  - pi0 - Proportion of positive samples in unlabeled set
  - alpha - The combination parameter of the confidence information term and the label information term
  - lambda - The regularization parameter

  and returns:
  - model - A (d+1)x1 array, linear-in-parameter model
* demo.m: script that you can directly run on synthetic dataset sample.mat.

## Contact:
If there are any problems, please feel free to contact Xijia Tang(TXJnudt@hotmail.com).
