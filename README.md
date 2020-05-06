# 中州韻粵語拼音輸入法分歧拼音系統補丁
* 依賴於：[`rime/rime-cantonese`](github.com/rime/rime-cantonese)
* 呢個補丁將`jyut6ping3*.dict.yaml`嘅詞句轉換成其他主流拼音系統，方便用開非「粵拼」拼音系統嘅用家使用。
* **長遠請考慮轉用香港語言學學會嘅粵語拼音方案（「粵拼」），一嚟比較貼近國際音標，二嚟大部分嘅現代粵語資源都係用「粵拼」標音。如果閣下希望同本地粵語文化接軌，請考慮轉用粵拼。**

## 我用緊邊種拼音系統？
 你會將「出」字拼成... | 拼音系統  | 方案詳情 | 常見於（純粹主觀感覺）
 :-------------: | ------------- | --------- | --------
 ceot       | **粵拼** (/œː/作`oe`，/ɵ/作`eo`)| [呢到](https://zh.wikipedia.org/zh-hk/%E9%A6%99%E6%B8%AF%E8%AA%9E%E8%A8%80%E5%AD%B8%E5%AD%B8%E6%9C%83%E7%B2%B5%E8%AA%9E%E6%8B%BC%E9%9F%B3%E6%96%B9%E6%A1%88) | 現代學術資料，社羣粵語資料，字典
 cheut      | **耶魯拼音** (/œː/、/ɵ/ 一律作`eu`)| [呢度](https://zh.wikipedia.org/wiki/%E8%80%B6%E9%AD%AF%E6%8B%BC%E9%9F%B3#%E7%B2%A4%E8%AF%AD%E8%80%B6%E9%B2%81%E6%8B%BC%E9%9F%B3) | 上世紀學術資料，Gboard等輸入法
 coet       | **教院式拼音** (/œː/、/ɵ/ 一律作`oe`)| [呢度](https://zh.wikipedia.org/wiki/%E6%95%99%E8%82%B2%E5%AD%B8%E9%99%A2%E6%8B%BC%E9%9F%B3%E6%96%B9%E6%A1%88) | 教育局資料
 chut       | **劉錫祥式拼音** (/œː/作`eu`，/ɵ/作`u`) | [呢度](https://zh.wikipedia.org/wiki/%E5%8A%89%E9%8C%AB%E7%A5%A5%E6%8B%BC%E9%9F%B3) | 外國粵語社羣，面向外國人嘅粵語教材

## 安裝方法
1. [下載呢個程式庫](https://github.com/tanxpyox/rime-cantonese-schemes/archive/master.zip)，然後解壓縮。
2. 揀啱你用開嘅拼音方案，將入面個`jyut6ping3.custom.yaml`放入去[RIME「用戶資料夾」](https://github.com/rime/home/wiki/UserData)度。
3. 重新部署
