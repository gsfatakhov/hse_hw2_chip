# HW 2 
## Фатахов Георгий группа 1
#### Выбрана клеточная линия `A549` и гистоновая метка `H3K4me2`

[Ноутбук]()

### FastQC

ChipSeq реплики:
1. [ENCFF584XSR](data/ENCFF584XSR_fastqc.html)
2. [ENCFF549USR](data/ENCFF549USR_fastqc.html)

Контроль: 
- [ENCFF047IPB](data/ENCFF047IPB_fastqc.html)


### Сравнение

#### Basic Statistics
![alt text](data/XSR_bs.png)
![alt text](data/USR_bs.png)
![alt text](data/IPB_bs.png)

#### Per base sequence quality

![alt text](data/XSR_pbsq.png)
![alt text](data/USR_pbsq.png)
![alt text](data/IPB_pbsq.png)

#### Per sequence quality scores
![alt text](data/XSR_psqs.png)
![alt text](data/USR_psqs.png)
![alt text](data/IPB_psqs.png)

#### Per base sequence content
![alt text](data/XSR_pbsq.png)
![alt text](data/USR_pbsq.png)
![alt text](data/IPB_pbsq.png)


#### Per sequence GC content
![alt text](data/XSR_psgcc.png)
![alt text](data/USR_psgcc.png)
![alt text](data/IPB_psgcc.png)

#### Per base N content
![alt text](data/XSR_pbnc.png)
![alt text](data/USR_pbnc.png)
![alt text](data/IPB_pbnc.png)

Заметим что Фильтрация и подрезания не требуются.

### Выравнивание на 17 хромосому


id | Число всех ридов | Выровнившиеся уникально (шт, %) | Выровнившиеся неуникально (шт, %) | Не выровнившиеся (шт, %) 
--- | --- | --- | --- | ---
ENCFF584XSR | 43444925 | 2327083 (5.36%) | 4436205 (10.21%)| 36681637 (84.43%)
ENCFF549USR | 41468651 | 2453765 (5.92%) | 3835766 (9.25%) | 35179120 (84.83%)
ENCFF047IPB | 28485184 | 1219728 (4.28%) | 3110068 (10.92%)| 24155388 (84.80%)


### Диаграммы Эйлера-Венна

#### Пересечения пиков `ENCFF584XSR` и `ENCODE`

`ENCFF584XSR` c `ENCODE`
![alt text](data/XSR_ENCODE.png)

`ENCODE` c `ENCFF584XSR`
![alt text](data/ENCODE_XSR.png)

#### Пересечения пиков `ENCFF549USR` и `ENCODE`

`ENCFF549USR` c `ENCODE`
![alt text](data/USR_ENCODE.png)

`ENCODE` c `ENCFF549USR`
![alt text](data/ENCODE_USR.png)


#### Вывод

Получили маленькое пересечение, т.к. выравнивание было сделано только на одну хромосому.
ENCODE пиков намного больше т.к. они получены для всех хромосом. Важно отметить, что пересечение полученных пиков с ENCODE и пересечение ENCODE пиков с полученными это не одно и то же (соответвсвенно значения различаются).
