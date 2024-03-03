# hse_hw2_chip
### Варфоломеева Анастасия Андреевна БПМ213

[Ссылка на основной гугл коллаб](https://colab.research.google.com/drive/1pwT_Rmg8sMyn3SFuWB54xriAFRb5DczN?usp=sharing)
[Ссылка на гугл коллаб с построением диаграммы вена](https://colab.research.google.com/drive/1j6KlN21ORVTwubk47X0LsJHUHS5rgzas?authuser=1#scrollTo=U-QNPFitX1du)


Клеточная линия | Гистоновая метка | Реплика 1 | Реплика 2 | Контроль 
--- | --- | --- | --- | ---
PC-9 | H3K79me2 | ENCFF392RHX | ENCFF197OPO | ENCFF163PYU


## Отчеты Fastqc
 
   При анализе Fastqc подрезание не потребовалось. Как видно из приведенных ниже скриншотов у файлов почти все параметры в норме, так что подрезание с помощью программы trimmomatic не понадобилось. Summery говорит о том, что всего 2-3 параметра немного не в норме. В теории значения аминокислот должны колебаться в районе 25%, что не сильно отличается от нашего случая. Распределение не сильно отличается от теоретического.

ENCFF392RHX | ENCFF197OPO | ENCFF163PYU 
--- | --- | --- 
![](https://github.com/switerElly/hse_hw2_chip/blob/main/img/Screenshot%20from%202024-03-02%2022-05-21.png) | ![](https://github.com/switerElly/hse_hw2_chip/blob/main/img/Screenshot%20from%202024-03-02%2022-05-25.png) | ![](https://github.com/switerElly/hse_hw2_chip/blob/main/img/Screenshot%20from%202024-03-02%2022-05-27.png)
--- | --- | --- 
![](https://github.com/switerElly/hse_hw2_chip/blob/main/img/Screenshot%20from%202024-03-03%2016-28-29.png) | ![](https://github.com/switerElly/hse_hw2_chip/blob/main/img/Screenshot%20from%202024-03-03%2016-28-34.png) | ![](https://github.com/switerElly/hse_hw2_chip/blob/main/img/Screenshot%20from%202024-03-03%2016-28-49.png)
--- | --- | --- 
![](https://github.com/switerElly/hse_hw2_chip/blob/main/img/Screenshot%20from%202024-03-03%2016-31-13.png) | ![](https://github.com/switerElly/hse_hw2_chip/blob/main/img/Screenshot%20from%202024-03-03%2016-31-18.png) | ![](https://github.com/switerElly/hse_hw2_chip/blob/main/img/Screenshot%20from%202024-03-03%2016-31-25.png)

 Из данных табличек можем сделать вывод, что большинство анализов проведены корректно и с ними можно работать.

## Таблица со статистикой по каждому из 3 образцов

|  | **Реплика 1 (ENCFF392RHX)** | **Реплика 2 (ENCFF197OPO)** | **Контроль (ENCFF163PYU)** |
| ------------- | ------------- |--------------------| ---- |
| Всего ридов | 46752135 | 28444872 | 17667656 |
| Выравнилось уникально | 2695935 (5.77%) | 1656621 (5.82%) | 1009460 (5.71%) |
| Выравнилось НЕ-уникально | 4618763 (9.88%) | 2902889 (10.21%) | 1667554 (9.44%) |
| НЕ выравнилось | 39437437 (84.35%) | 23885362 (83.97%) | 14990642 (84.85%) | 

Процент выравнивания получился столь низким из-за того, что оно проводилось только на одну хромосому.

## Диаграммы Венна
   
Для реплики 1 (ENCFF392RHX)
Количество участков для реплики 1 и ENCFF279CPR  | Количество участков для ENCFF279CPR и реплики 1
--- | --- 
![](https://github.com/switerElly/hse_hw2_chip/blob/main/img/Intervene_venn.pdf) | ![](https://github.com/switerElly/hse_hw2_chip/blob/main/img/Intervene_venn%20(1).pdf)
     
Для реплики 2 (ENCFF197OPO)
Количество участков для реплики 2 и ENCFF279CPR  | Количество участков для ENCFF279CPR и реплики 2
--- | --- 
![](https://github.com/switerElly/hse_hw2_chip/blob/main/img/Intervene_venn%20(2).pdf) | ![](https://github.com/switerElly/hse_hw2_chip/blob/main/img/Intervene_venn%20(3).pdf)

Из диаграмм видно, что у нас не очень большое количество пересечений. Это можно объяснить следующим: в наших репликах было небольшое количество пиков из-за выравнивания только на одну хромосому, в то время как образец из ENCODE был выровнен на все хромосомы, так что имел много пиков. В пересечении одних и тех же файлов разное, ведь кличество пиков из одного файла, которые есть во втором файле != количеству пиков из второго файла, которые есть во первом. 


## Бонусная часть

![](https://github.com/switerElly/hse_hw2_chip/blob/main/img/Screenshot%20from%202024-03-03%2020-05-22.png)

Heatmap для .bam файлов и соотвествующих им .bigWig файлов
  
ngs.plot для ENCFF347OCC.bam | ngs.plot для ENCFF636MHF.bam
--- | --- 
![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/NIR.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/UVW.png)
     
Полученные графики для .bam файлов похожи на типичное расположение гистоновой метки относительно генов. Наш график имеет сильно похожее на теоретическое расположение (рисунок выже).
