# hse_hw3_chromhmm
### _Сушкова Дарья Сергеевна, подгруппа 2_
#### [Ссылка на Google Colab](https://colab.research.google.com/drive/1wkV56kkF3-7NGExJ0GT5kOHI0GmDAyus?usp=sharing)
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
![image](https://user-images.githubusercontent.com/89806836/230183945-bd162416-a1a3-4221-9b45-51f78a0d755a.png)      
#### UCSC GenomeBrowser
Использовался файл Huvec_10_dense.bed. Настройка панели с профилями гистоновых модификаций, на основании которых были определены эпигенетические пики:   
![image](https://user-images.githubusercontent.com/89806836/229349573-8916cc24-916e-4634-a7a6-4460c888c983.png)   
Изображения из геномного браузера для различных участков генома с учетом эпигенетических типов и профилей эпигенетических меток:
![gen_firts](https://user-images.githubusercontent.com/89806836/229630232-431048a4-782d-4fa6-aa03-88aac1a58e95.png)   
![second_gen](https://user-images.githubusercontent.com/89806836/229630263-887ff64f-cb9a-41a6-856d-c21fd3e5dbdd.png)   
![third_gen](https://user-images.githubusercontent.com/89806836/229630305-1401cdb1-05ae-4945-b1da-9ce293b29de4.png)   
#### Табличка эпигенетических типов
_Примечание:_ в табличке используется условная нотация "+/-/+-", которая ассоциирована с расположением гистоновых модификаций относительно различных категорий.
Выводы о наименованиях делались на основании выдачи $ChromHMM,$ данных $UCSC$ и дополнительной литературы в Интернете.
Состояние | Название типа | Метки | CpG островки | TSS | TES | Lamina | Саммари
--- | --- | --- | --- | --- | --- | --- | ---
1 | Transcribed | H3K4me1, H3K79me2, немного H3K9me3 | - | - | Ярко выражено на всем промежутке, больше до | +- | Редко встречается на геноме, попадает на интроны, сильные сигналы для H3K4me1 и H3K79me2 - ассоциация с транскрибируемыми областями активных генов, сильная ассоциация с SeqGene и TES
2 | Transcribed | H3K4me1, H3K79me2, немного H3K9me3, H4K20me1 | - | - | Очень слабо выражено на всем промежутке, больше до | - | Cильные сигналы для H3K79me2 - ассоциация с транскрибируемыми областями активных генов, сильная ассоциация с SeqGene, попадает на интроны 
3 | Transcribed | H3K4me1, H3K4me2, H3K4me3, H3K79me2, H3K9me3, H4K20me1, H3K9ac, H3K27me3, H3K27me3 | - | На граничных позициях, больше после | Слабо выражено на всем промежутке, больше до | - | Редко встречается в геноме, сильные сигналы для H3K4me1 и H3K79me2 - ассоциация с транскрибируемыми областями активных генов, сильная ассоциация с SeqGene, попадает на интроны
4 | Enhancer | H3K4me1, H3K4me2, H3K27me3, H3K9me3 | - | Слабо на граничных позициях | Слабо выражено на всем промежутке | +- | Редко встречается в геноме, сильный сигнал для H3K4me1 - явная ассоциация с усилителями генов
5 | Strong enhancer | H3K4me1, H3K4me2, H3K4me3, H3K9ac, H3K27ac, H3K79me2 | - | Слабо на граничных позициях | Слабо выражено на всем промежутке | +- | Редко встречается в геноме, сильный сигнал для всех указанных меток (но наиболее сильный для H3K4me1 - ассоциация с усилителями генов), расположен на интроне, небольшая ассоциация с TES 
6 | Active Promoter | H3K4me1, H3K4me2, H3K4me3, H3K9ac, H3K27ac, H3K79me2 | + | Ярко выражено на TSS, спады на границах | Ярко выражено на всем промежутке, больше до | - | Редко встречается в геноме, сигнал сильный (особенно для H3K4me2 и H3K4me3 - наибольшее обогащение в начале транскрипции), ассоциация с TES и TSS 
7 | Active Promoter | H3K4me2, H3K4me3, H3K9ac, H3K27ac, H3K79me2 | + | Выражено на TSS, спады на границах | Выражено на всем промежутке | +- | Редко встречается в геноме, сильный сигнал для H3K4me2 и H3K4me3 (наибольшее обогащение в начале транскрипции), ассоциация с TES и TSS
8 | Heterochromatin |  H3K9ac, H3K27me3 | +- | Очень слобо выражено на всем промежутке | Слабо выражено на всем промежутке | + | Много в геноме, не попадает на ген, в целом слабый сигнал (наиболее сильный для H3K27me3 - ассоциация с гетерохроматическими областями)
9 | Heterochromatin |  H3K4me1, H3K9me3, H3K27me3 | - | - | Очень слабо выражено на всем промежутке | + | Больше всего в геноме, в целом слабый сигнал (наиболее сильный для H3K27me3 - ассоциация с гетерохроматическими областями), попадает на интрон
10 | Heterochromatin | H3K9me3, немного H3K27me3, H3K79me2 | - | - | - | + | На интроне, сильный сигнал для H3K9me3 (частая ассоциация с гетерохроматином)
#### Список запущенных команд
_Примечание:_ чтобы не загромождать пространство, автор решил предоставить в файле $README$ только часть команд, которые имеют смысловую нагрузку. Остальные каманды (установка java и ChromHMM) предоставлены в ноутбуке Google Colab:    
1) Скачивание файлов:
```
# Скачивание файла с контрольным экспериментом.
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHepg2ControlStdAlnRep1.bam -O ControlStdAlnRep1.bam

# Скачивание выравнивания для модификаций гистонов (10 штук).
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHepg2H3k27acStdAlnRep1.bam -O H3k27acStdAlnRep1.bam
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHepg2H3k27me3StdAlnRep1.bam -O H3k27me3StdAlnRep1.bam
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHepg2H3k36me3StdAlnRep1.bam -O H3k36me3StdAlnRep1.bam
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHepg2H3k04me1StdAlnRep1.bam -O H3k04me1StdAlnRep1.bam
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHepg2H3k4me2StdAlnRep1.bam -O H3k4me2StdAlnRep1.bam
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHepg2H3k4me3StdAlnRep1.bam -O H3k4me3StdAlnRep1.bam
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHepg2H3k79me2StdAlnRep1.bam -O H3k79me2StdAlnRep1.bam
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHepg2H3k9acStdAlnRep1.bam -O H3k9acStdAlnRep1.bam
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHepg2H3k09me3AlnRep1.bam -O H3k09me3AlnRep1.bam
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHepg2H4k20me1StdAlnRep1.bam -O H4k20me1StdAlnRep1.bam
```
2) BinarizeBam:   
```
! java -mx5000M -jar /content/ChromHMM/ChromHMM.jar BinarizeBam -b 200  /content/ChromHMM/CHROMSIZES/hg19.txt /content/ cellmarkfiletable.txt   binarizedData
```
3) LearnModel:   
```
! java -mx5000M -jar /content/ChromHMM/ChromHMM.jar LearnModel /content/binarizedData LearnModelOutput 10 hg19
```
4) Скачивание выгрузки ChromHMM:   
```
! zip -r learmodel.zip LearnModelOutput/
```
#### Бонусная часть
Код бонусной части (также есть в ноутбуке Google Colab):   
```
import pandas as pd

header = ['chrom', 'start', 'end', 'state', 'zero', 'dot', 'start_1', 'end_1', 'rgb']
df = pd.read_csv('Huvec_10_dense.bed', sep='\t', skiprows=1, header=None, names=header)

df.loc[df.state == 1, 'state'] = '1_Transcribed'
df.loc[df.state == 2, 'state'] = '2_Transcribed'
df.loc[df.state == 3, 'state'] = '3_Transcribed'
df.loc[df.state == 4, 'state'] = '4_Enhancer'
df.loc[df.state == 5, 'state'] = '5_Strong_Enhancer'
df.loc[df.state == 6, 'state'] = '6_Active_Promoter'
df.loc[df.state == 7, 'state'] = '7_Active_Promoter'
df.loc[df.state == 8, 'state'] = '8_Heterochromatin'
df.loc[df.state == 9, 'state'] = '9_Heterochromatin'
df.loc[df.state == 10, 'state'] = '10_Heterochromatin'

df.to_csv('Huvec_10_dense_new.bed', sep='\t', index=False, header=None)
```   
Например, теперь иллюстрация выглядит так, что действительно более читабельно:   
   
![bonus](https://user-images.githubusercontent.com/89806836/230200787-1ee5795e-bd5c-45f3-b5ba-73ed505266b5.png)   
