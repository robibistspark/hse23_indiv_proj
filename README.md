## Реепозиторий с индивидуальной частью задания по проекту об эволюции эпигенетики 
Использованный код доступен в .ipynb файле. Выполнялся на сервере и локально (со своими библиотеками).

### Описание белка
Белок NP_001230715.1, получающийся по гену RAG2 (https://genome.ucsc.edu/cgi-bin/hgc?hgsid=1640679168_uQmWgXNxlLN40x5fVJEmMjNxb0Y3&db=hg19&c=chr11&l=36607155&r=36626166&o=36613492&t=36619786&g=ncbiRefSeqCurated&i=NM_001243786.2). Этот ген участвует в чтении метилирования H3K4Me, согласно таким статьям, как 1) https://www.pnas.org/doi/abs/10.1073/pnas.0709170104 и 2) https://www.nature.com/articles/nature06431. В организме человека экспрессируется почти только в щитовидной железе (RPKM 16.6), но также понемногу в семенниках и костном мозге, согласно NCBI.

### Выравнивания гистонов
Выравнивания я делал в локальной MEGAX с помощью алгоритма MUSCLE (через UPGMA). Результаты в виде файлов загружены в репозиторий, ниже привожу скриншоты, на которых видны основные вещи.
#### H2A
![image](https://github.com/robibistspark/hse23_indiv_proj/assets/71763293/4756f783-466b-4289-91cf-9af139bd537d)
На первый взгляд мы видим сильн отличающиеся варианты, но на самом деле дело в том, что в файле имеется две серии последовательностей: MACRO H2A и "обычные" H2A. Каждая серия представлена вариантами с небольшим числом замен - видимо, синонимичных (или просто не имеющих значение).

#### H2B
![image](https://github.com/robibistspark/hse23_indiv_proj/assets/71763293/e89267d0-b52f-4838-abc4-097e883a94db)
Некоторые варианты генов этого гистона отличаются вставками, но весьма короткими и, вероятно, синонимичными (или просто не имеющими значение).

#### H3
![image](https://github.com/robibistspark/hse23_indiv_proj/assets/71763293/b41a49a7-e226-4779-8eca-0f8a3a63a3f2)
Все варианты среди генов этого гистона отлично выравниваются.

#### H4
![image](https://github.com/robibistspark/hse23_indiv_proj/assets/71763293/85859ce5-1dd6-4627-9a45-1981cfa78565)
Все варианты среди генов этого гистона тоже отлично выравниваются.

### Таблички и хитмэп
#### Табличка e-value (raw)
![image](https://github.com/robibistspark/hse23_indiv_proj/assets/71763293/49a9b788-aed4-4f69-91a2-9c6bf6026752)

#### Табличка -log(e-value) (natural logarithm)
![image](https://github.com/robibistspark/hse23_indiv_proj/assets/71763293/fce1fdb0-f9a4-499c-82b8-842d5c7fa1c5)

#### Хитмэп последней таблички
![image](https://github.com/robibistspark/hse23_indiv_proj/assets/71763293/7905ae5d-ff76-44ed-894c-9a19f8c201fd)

### Вывод о появлении в эволюции
Наибольшее сходство в искомом белке наблюдается у многоклеточных позвоночных организмов, а у более "архаичных" организмов сходство очень незначительное. Можно сделать вывод о том, что мой белок (и его ген) появился в эволюции достаточно поздно, а именно, по-видимому, у позвоночных.
