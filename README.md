# CURED

<p align="center">
    <img src="https://github.com/totalintelli/dhh_2020/blob/master/logo3.png?raw=true" alt="cureD logo" width="200" height="200">
</p>

  CURED is software that applies the rare cancer drug treatment decision-making AI model.<br/>
  CURED는 희귀암 약물 치료 의사 결정 AI 모델을 적용한 소프트웨어입니다.
   
 
* * *


## Table of Contents

- [Project Introduction](#Project-Introduction)
- [Dependencies](#Dependencies)
- [Rule](#Rule)
- [About the Contributor](#About-the-Contributor)
- [License](#License)


## Project Introduction

### 희귀암 약물 치료 의사 결정 AI 모델

 - 약물 치료의 효과는 환자 개인의 특성에 따라 다르게 나타납니다. 현재까지는 평균적인 효과에 맞추어 치료를 하지만, 실제로 어떤 특정 환자에게는 효과가 없거나, 치명적인 부작용을 야기합니다.
- 의료 빅데이터는 이러한 치료 결과에 대한 대량의 정보를 제공합니다. 의료 빅데이터를 통해 환자 개인의 특성에 따른 맞춤형 치료가 가능합니다.
- 환자들이 가지고 있는 다양한 변수와 편향된 과거 데이터를 이용하여 치료 효과에 대한 인과관계를 찾는 것은 매우 어렵습니다. 과거 데이터를 이용하여 치료가 적합한 사람과 적합하지 않은 사람을 구별합니다. CURED는 의사에게 치료가 적합한 사람과 그렇지 않은 사람을 구별할 수 있도록 돕는 의사 결정 보조 인공지능입니다.



## Dependencies
- OS : Windows10
- Language : Python
- Library : Tensorflow 2.3.0, Keras 2.4.3
- Editor : Jupyter notebook 

## Rule

### [데이터 셋](https://www.digitalhealthhack.org/ai-1)

- Training Data
  - trainX.csv
    - 0 ~ 1 사이의 continuous data이며, 환자들의 상태를 표현합니다.
    - X0~X16까지의 column, 17개의 변수로 구성되며 이는 환자의 개인별 상태를 반영합니다.
    - 이 중 일부는 교란 변수로 존재하여 치료에 영향을 주는 동시에 환자의 최종 생존 기간 (Y)에 영향을 줍니다.
    - 이 데이터에서 시행된 치료(T)는 의료진에 의하여 임의로 진행되었으며, 치료 당시 여러 변수가 고려되었지만, 반드시 최적의 치료라고 보기는 어렵습니다.

   - trainY.csv
      - 개별 환자의 최종 생존 기간을 나타내며 time, event의 2개의 column이 있습니다.
      - 최종 생존 기간은 의료진이 관심있는 이 치료의 최종 목표이며 적절한 환자에게 치료한 경우 생존기간이 연장 될 수 있지만, 어떤 환자에게 이 치료법은 생존기간을 단축 시킵니다.
      - time은 음수가 아닌 continuous data로서 환자의 생존 시간입니다.
      - event는 binary data로서 1은 환자의 event발생, 0은 censored 입니다. (본 데이터에서는 분석의 편의상 censored data는 없는 것으로 하였습니다.)
      
    - trainA.csv
      - binary data이며, treatment (T) 즉 치료 여부를 의미합니다.
      - 과거에 어떻게 치료하였는가에 대하여 표현합니다.(이것이 정답을 뜻하진 않습니다. 잘 치료된 경우도 있고, 잘 못해서 생존이 오히려 줄어든 경우도 있을 겁니다.)
      - 1은 치료한다, 0은 치료하지 않는다를 뜻합니다.
      
- Test Data
  - testX.csv
    - trainX.csv와 형식은 같은 test data입니다.

## About the Contributor

**Hyung Jo Yang**
- [**@**](https://github.com/)   
- <xxx@gmail.com>  

**Yekaterina Kim**
- [**@**](https://github.com/)
- <xxx@gmail.com>

**Yong Dan Song**
- [**@totalintelli**](https://github.com/totalintelli)
- <blueintelli@gmail.com>

### License

CURED is [MIT licensed](./LICENSE).

* * *
