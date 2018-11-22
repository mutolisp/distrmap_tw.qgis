# distrmap_tw.qgis
Horizontal and vertical species distribution map of Taiwan

物種的水平及垂直分布圖 QGIS 專案範本檔

[![DOI](https://zenodo.org/badge/82152043.svg)](https://zenodo.org/badge/latestdoi/82152043)


這個版本庫是 QGIS 繪製物種分布的水平和垂直剖面的範本檔，內容包含了相關所需之圖層以及 .qgs 專案檔。
輸出結果請參見下圖：

![](https://github.com/mutolisp/distrmap_tw.qgis/raw/master/docs/output_distr_map.png)

## 預先安裝

請先安裝好 [QGIS 3.x](https://qgis.org)

## How-To

1. 請先下載這個 [repository](https://github.com/mutolisp/distrmap_tw.qgis/archive/master.zip) 並解壓縮
2. 壓縮檔內附有範例檔案([csv](https://github.com/mutolisp/distrmap_tw.qgis/raw/sample_pts.csv)、[ods](https://github.com/mutolisp/distrmap_tw.qgis/raw/sample_pts.ods)、[xlsx](https://github.com/mutolisp/distrmap_tw.qgis/raw/sample_pts.xlsx))，您可以使用 [LibreOffice](http://libreoffice.org) 或是 [Google Docs](https://docs.google.com) 開啟，檔案長的像這樣：

|longitude | latitude | elevation | vert_elevation |
|----------|----------|-----------| -------------- |
|121.195   | 23.947   | 1280      |         122.42 |
|121.282   | 24.026   | 2606      |       122.7515 |
|121.310   | 24.230   | 2120      |         122.63 |

或是請您先準備好相同格式的資料，至少有四個欄位：經度、緯度、海拔高度以及垂直剖面高度座標（即在上表中的 ```vert_elevation```）。
vert_elevation 的換算公式為

```
v = 122.1 + L*0.9/3600
```
其中 v 為 ```vert_elevation```，L 為海拔高度，若您使用試算表軟體，可在 ```vert_elevation``` 這個欄位中輸入(假設海拔高度是在 A2 儲存格中)：
```
=122.1 + A2*0.9/3600
```
3. 將您要顯示的座標修改並貼在這個試算表中，請記得存檔時務必存成 csv 格式，即：```sample_pts.csv``` (可以覆蓋範例檔，但請保留欄位名稱）

4. 在 QGIS 中開啟 [vertProfileTW.qgs](https://github.com/mutolisp/distrmap_tw.qgis/raw/vertProfileTW.qgs) 這個檔案

5. 從選單中選取 Projects -> Layouts -> Distribution map

6. 選擇輸出成 pdf 或 png 即可（請參考下圖或 QGIS 文件）

![](https://github.com/mutolisp/distrmap_tw.qgis/raw/master/docs/export_distr_map.png)

## License 授權

[![CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## Citation 引用

中文引用

林政道 (2018) 物種的水平及垂直分布圖 QGIS 專案範本檔。URL: https://github.com/mutolisp/distrmap_tw.qgis. DOI: 10.5281/zenodo.1493690

English citation

Cheng-Tao Lin (2018) QGIS template for diplaying species distribution by horizontal and vertical view in Taiwan. URL: https://github.com/mutolisp/distrmap_tw.qgis. DOI: 10.5281/zenodo.1493690
