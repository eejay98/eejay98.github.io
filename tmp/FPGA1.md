---
title: "FPGA 1"
---

## Optimizing FPGA-based Accelerator Design for Deep Convolutional Neural Networks (FPGA '15)

&nbsp;&nbsp;이 논문에서는 좋은 성능을 유지하되 적은 리소스를 사용하는 FPGA 기반 딥러닝 가속에 관한 솔루션을 제공한다. 
딥러닝 가속기 설계를 위해 배경 지식을 쌓으면서 FPGA 딥러닝 가속기 관련 survey 논문들을 찾아 공부하다가 언급이 많이 되어 찾아 읽게 되었다.

### Introduction

&nbsp;&nbsp;이 논문과 같이 FPGA 딥러닝 가속기를 다루거나 기존 딥러닝 알고리즘을 간소화 및 최적화를 하는 논문들의 introduction은 항상 같은 레퍼토리로 진행을 한다. 
기존의 딥러닝, 특히 CNN은 layer의 개수를 늘려 높은 정확도를 얻어내는 것에 집중했다. 
그러나 layer가 많아질수록 연산량이 많아져 training에 걸리는 시간은 물론, inference하는 시간 또한 증가한다. 
이 시간을 줄이는 데에 가장 적절한 것이 바로 **FPGA**이다. 
FPGA의 좋은 성능, 높은 효율, 무엇보다도 빠른 개발 시간과 reconfiguration의 가능성 때문에 연구자들은 GPU보다 FPGA를 선호한다. 
이 논문에서는 기존에 computation engine의 최적화에 주로 집중을 하던 기존 논문들과 다르게 buffer management와 bandwidth optimization를 적용하여 통해 더 좋은 성능을 얻어낸다. 
또한 서로 다른 layer에 대해 reconfigure할 필요 없이 잘 가속할 수 있는 솔루션을 제공한다.

### Background

&nbsp;&nbsp;
