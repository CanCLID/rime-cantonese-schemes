## 安裝方法
1. 打開terminal
2. 輸入以下指令
```sh
bash rime-install tanxpyox/rime-cantonese-schemes:install:scheme=yale
```
其中`yale`可轉爲其他羅馬拼音嘅名稱：

| 羅馬拼音方案 | 項目指令     |
| :------------- | :------------- |
| 耶魯       | `yale`       |
| 教院       | `edu`       |
| 黃錫凌       | `wong`       |
| 劉錫祥       | `lau`       |

3. 重新部署

又或者以下載覆蓋方式安裝指令：（註：其他補丁可能因此而被覆蓋）

1. [下載呢個程式庫](https://github.com/tanxpyox/rime-cantonese-schemes/archive/master.zip)，然後解壓縮。
2. 揀啱你用開嘅拼音方案，將入面個`jyut6ping3.custom.yaml`放入去[RIME「用戶資料夾」](https://github.com/rime/home/wiki/UserData)度。
3. 重新部署。

## 解安裝方法
1. 入去[RIME「用戶資料夾」](https://github.com/rime/home/wiki/UserData)度。
2. 刪除`jyut6ping3.custom.yaml`。
3. 重新部署。
