# hse_hw2_chip
### Варфоломеева Анастасия Андреевна БПМ213

[Ссылка на гугл коллаб](https://colab.research.google.com/drive/1pwT_Rmg8sMyn3SFuWB54xriAFRb5DczN?usp=sharing)


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
| Всего ридов | 25022209 | 28444872 | 17667656 |
| Выравнилось уникально | 21345405 (85.31%) | 1656621 (5.82%) | 1009460 (5.71%) |
| Выравнилось НЕ-уникально | 953167 (3.81%) | 2902889 (10.21%) | 1667554 (9.44%) |
| НЕ выравнилось | 2723637 (10.88%) | 23885362 (83.97%) | 14990642 (84.85%) | 

Процент выравнивания получился столь низким из-за того, что оно проводилось только на одну хромосому.
