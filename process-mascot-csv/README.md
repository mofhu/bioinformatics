# mascot-csv-process

Processing .csv file generated by Mascot by Python

Author: Frank Hu (Frank-the-Obscure@GitHub)

## How to use

Install Python 3 (Python 3.4 is used to create and test this project)

There are three ways to use this tool.

## 1. extract-input-folder.py
Let user input the directory. Extract all available .csv files in that directory. Output to `combined.csv` in that directory.
**Example**
```
$ python extract-input-folder.py
Please input folder path(e.g. D:\Study\Inbox): C:\Users\Hu\Documents\GitHub\masc
ot-csv-process\csv test
input directory is:  C:\Users\Hu\Documents\GitHub\mascot-csv-process\csv test

output to "combined.csv".
read 4 files, output 2367 lines
```

## 2. extract-all.py
Automatically extract all available .csv files in the same folder of `extract-all.py`. Output to `combined.csv` in that directory.

**Example: when two files are in the folder**
```
$ python extract-all.py
input dir is:  C:\Users\Hu\Documents\GitHub\mascot-csv-process

output to "combined.csv".
read 2 files, output 887 lines
```

## 3. extract.py
Copy .csv files to the folder contains `extract.py`.

Run `extract.py` and follow instructions.

Note that this script only recognize uniprot format data now (with 'OS=' string in the annotation).

**Example: combine three files**

```
$ python extract.py
Please input file name (without ".csv"), input s to finish: F006005
F006005
enter name ok
"D:\Data\Hu\20150224Shigella_in-vivo\1\1ex1.raw"
584
Please input file name (without ".csv"), input s to finish: F006006
F006006
enter name ok
"D:\Data\Hu\20150224Shigella_in-vivo\1\1ex2.raw"
1165
Please input file name (without ".csv"), input s to finish: F006007
F006007
enter name ok
"D:\Data\Hu\20150224Shigella_in-vivo\1\1ex3.raw"
1846
Please input file name (without ".csv"), input s to finish: s
s
output finished. out put 1846 lines

```

## 4. mgf file extraction
Extract specific MS/MS spectra from mgf file.

---

Chinese note

有三种方式导出 Mascot 的 .csv 文件

1. extract-input-folder.py 输入目录名称, 自动导出该目录下所有文件至 combined.csv
2. extract-all.py 导出脚本当前目录下的所有文件至 combined.csv
3. extract.py 手动输入脚本当前目录下, 想要合并的csv文件.

mgf 文件提取

4. mgf_identified.py 提取 mgf 文件中的某些特定谱图(如被鉴定到的谱图, 通过 csv 文件输入指定).