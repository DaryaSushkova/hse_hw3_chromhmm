# hse_hw3_chromhmm
### _Сушкова Дарья Сергеевна, подгруппа 2_

#### Табличка с гистоновыми метками
Гистоновая метка | Имя файла
--- | --- 
H3K27ac | wgEncodeBroadHistoneHepg2H3k27ac
H3K27me3 | wgEncodeBroadHistoneHepg2H3k27me3
H3K36me3 | wgEncodeBroadHistoneHepg2H3k36me3
H3K4me1 | wgEncodeBroadHistoneHepg2H3k04me1
H3K4me2 | wgEncodeBroadHistoneHepg2H3k4me2
H3K4me3 | wgEncodeBroadHistoneHepg2H3k4me3
H3K79me2 | wgEncodeBroadHistoneHepg2H3k79me2
H3K9ac | wgEncodeBroadHistoneHepg2H3k9ac
H3K9me3 | wgEncodeBroadHistoneHepg2H3k09me3
H4K20me1 | wgEncodeBroadHistoneHepg2H4k20me1
#### Выдача ChromHMM
Картинки доступны при открытии файла webpage_10.html папки с выдачей ChromHMM.   
![image](https://user-images.githubusercontent.com/89806836/229347886-68367b16-3d02-487d-a649-3bcf3a1f4c6d.png)   
$Emission\ parametres$ демонстрирует, какие метки и для каких состояний наиболее типичны.   
![image](https://user-images.githubusercontent.com/89806836/229348043-bbe9c82a-9baf-447b-bbfa-03d32a5ea954.png)   
$Fold\ Enrichment$ предоставляет общую статистику по состояниям. Можно увидеть, что 9 состояния встречается в геноме чаще всего. 6 состояние ассоциировано с $TSS$ (дополнительно предоставлю картинку из выдачи ниже, которая относится непосредственно к $TSS$) и $CpGIslands,$ что может говорить о соответствии промоторам, то есть стартовой площадке для начала транскрипции.   
![image](https://user-images.githubusercontent.com/89806836/229348522-467a5edd-3f2b-485b-93b6-f9bc37b1334b.png)   
Остальные картинки менее информативны, поэтому отдельно расписывать их не буду, выдача доступна в папке.   
#### UCSC GenomeBrowser
Использовался файл Huvec_10_dense.bed. Настройка панели с профилями гистоновых модификаций, на основании которых были определены эпигенетические пики:   
![image](https://user-images.githubusercontent.com/89806836/229349573-8916cc24-916e-4634-a7a6-4460c888c983.png)   
