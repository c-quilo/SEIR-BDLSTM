# SEIR-BDLSTM
A non-intrusive reduced-order model of an epidemiological Susceptible - Exposed - Infected - Recovered - Susceptible (SEIRS) model. The SEIRS model is an idealised town following parameters reported in the UK during the COVID-19 pandemic.
The SEIRS model has two grops: Home (can't leave home) and Mobile. This is a digital twin of say SEIRS model, where we approximate the original model solution using a Bidirectional LSTM.

<img width="721" alt="SEIRS_2groups_v4 (1)" src="https://user-images.githubusercontent.com/55235161/110819310-f6ee3680-8285-11eb-8f19-884d365d3264.png">
Movement between compartments Susceptible (S), Exposed (E), Infectious (I) and Recovered (R), and groups Home (H) and Mobile (M) for the extended SEIRS model. The spatial variation is not represented here, just movement between compartments and groups. The movement between home and mobile groups is defined by Lambda.

![PredBiLSTM (1)](https://user-images.githubusercontent.com/55235161/110819487-24d37b00-8286-11eb-92e5-d1891f0103bb.png)
Predictive Bidirectional LSTM for a sequence of two time levels. Top-left: off-line bidirectional LSTM network. Bottom-right: data-correction of the prediction. The Best Linear Unbiased Estimation (BLUE) is used to data-correct the prediction of the network. One time level corresponds to 10 time-steps of the original SEIRS solution.

## Citing this work

If you use this code or these models in your work, please cite the accompanying paper:

```
@article{quilodran2021digital,
  title={Digital twins based on bidirectional LSTM and GAN for modelling COVID-19},
  author={Quilodr{\'a}n-Casas, C{\'e}sar and Silva, Vinicius Santos and Arcucci, Rossella and Heaney, Claire E and Guo, Yike and Pain, Christopher C},
  journal={arXiv preprint arXiv:2102.02664},
  year={2021}
}
```
