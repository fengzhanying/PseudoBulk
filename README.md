# PseudoBulk
Pseudo-bulk stragety to merge scRNA-seq and scATAC-seq and construct regulatory network

1. Installation:
```bash
wget https://github.com/fengzhanying/cRegulon/archive/master.zip
unzip master.zip
cd cRegulon-master
wget https://www.dropbox.com/s/0h1wxlu7iqheajo/cRegulon.tar.gz
tar -xzvf cRegulon.tar.gz
rm -rf Input Results
```
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
6. Merge all the cells to make pseudo RNA-seq and ATAC-seq data & construct regulatory network

```bash
source PS_PECA.sh RAd4 mm10
```
