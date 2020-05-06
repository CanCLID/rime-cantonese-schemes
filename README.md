# 中州韻粵語拼音輸入法分歧拼音系統補丁
* 依賴於：[`rime/rime-cantonese`](github.com/rime/rime-cantonese)
* 呢個補丁將`jyut6ping3*.dict.yaml`嘅詞句轉換成其他主流拼音系統，方便唔係用「粵拼」嘅用家使用RIME。
* **長遠請考慮轉用香港語言學學會嘅粵語拼音方案（「粵拼」），一嚟比較貼近國際音標，二嚟大部分嘅現代粵語資源都係用「粵拼」標音。如果閣下希望同本地粵語文化接軌，請考慮轉用粵拼。**
* 呢度嘅程式碼係都以補丁方式實現，唔會影響其他輸入法檔案。

## 我用緊邊種拼音系統？
拼音系統  | 「水」| 「獎」 | 「歡」 | 常見於（純粹主觀感覺）
 :-------------: | ------------- | -------- | ---- | -----
 [**粵拼**](https://zh.wikipedia.org/zh-hk/%E9%A6%99%E6%B8%AF%E8%AA%9E%E8%A8%80%E5%AD%B8%E5%AD%B8%E6%9C%83%E7%B2%B5%E8%AA%9E%E6%8B%BC%E9%9F%B3%E6%96%B9%E6%A1%88) | seoi | zoeng | fun| 現代學術資料，社羣粵語資料，字典
[**耶魯拼音**](https://zh.wikipedia.org/wiki/%E8%80%B6%E9%AD%AF%E6%8B%BC%E9%9F%B3#%E7%B2%A4%E8%AF%AD%E8%80%B6%E9%B2%81%E6%8B%BC%E9%9F%B3)|  seui | jeung | fun | 上世紀學術資料，Gboard等輸入法
[**教院式拼音**](https://zh.wikipedia.org/wiki/%E6%95%99%E8%82%B2%E5%AD%B8%E9%99%A2%E6%8B%BC%E9%9F%B3%E6%96%B9%E6%A1%88) | soey | dzoeng | fun |香港教育局教材
[**劉錫祥拼音**](https://zh.wikipedia.org/wiki/%E5%8A%89%E9%8C%AB%E7%A5%A5%E6%8B%BC%E9%9F%B3)| sui| jeung| foon| 外國嘅粵語轉寫，「網上廣東話輸入法」，面向外國人嘅粵語教材

## 安裝方法
1. [下載呢個程式庫](https://github.com/tanxpyox/rime-cantonese-schemes/archive/master.zip)，然後解壓縮。
2. 揀啱你用開嘅拼音方案，將入面個`jyut6ping3.custom.yaml`放入去[RIME「用戶資料夾」](https://github.com/rime/home/wiki/UserData)度。
3. 重新部署。

## 解安裝方法
1. 入去[RIME「用戶資料夾」](https://github.com/rime/home/wiki/UserData)度。
2. 刪除`jyut6ping3.custom.yaml`。
3. 重新部署。

## 授權條款
GNU較寬鬆公共授權條款（第三版）。詳細條款請參閱[LICENSE](https://github.com/tanxpyox/rime-cantonese-schemes/blob/master/LICENSE)。
