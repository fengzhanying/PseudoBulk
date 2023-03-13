# PseudoBulk
Pseudo-bulk stragety to merge scRNA-seq and scATAC-seq and construct regulatory network

1. Download the script:
```bash
wget https://github.com/fengzhanying/PseudoBulk/archive/master.zip
unzip master.zip
cd PseudoBulk-master
```
3. Download this file: https://drive.google.com/file/d/1xBtb-grjgyqypuMlcmaGRsEgFZVgRlhy/view?usp=share_link
4. Prepare scRNA-seq file in following format:
<table>
  <tr>
    <td>scRNA</td>
    <td>Cell1</td>
    <td>Cell2</td>
    <td>Cell3</td>
  </tr>
  <tr>
    <td>Gene1</td>
    <td>5</td>
    <td>0</td>
    <td>3</td>
  </tr>
  <tr>
    <td>Gene2</td>
    <td>0</td>
    <td>2</td>
    <td>0</td>
  </tr>
  <tr>
    <td>Gene3</td>
    <td>1</td>
    <td>0</td>
    <td>0</td>
  </tr>
</table>
5. Prepare scATAC-seq file in following format:
<table>
  <tr>
    <td>scATAC</td>
    <td>Cell1</td>
    <td>Cell2</td>
    <td>Cell3</td>
    <td>Cell4</td>
  </tr>
  <tr>
    <td>Peak1</td>
    <td>1</td>
    <td>0</td>
    <td>1</td>
    <td>0</td>
  </tr>
  <tr>
    <td>Peak2</td>
    <td>0</td>
    <td>1</td>
    <td>0</td>
    <td>1</td>
  </tr>
  <tr>
    <td>Peak3</td>
    <td>1</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
</table>
The peaks are in the format of "chr_start_end". <br>
6. Merge all the cells to make pseudo RNA-seq and ATAC-seq data
```bash
python3 PseudoBulk.py
```
7. Run PECA to construct regulatory network
```bash
source PECA.sh RAd4 mm10
```
