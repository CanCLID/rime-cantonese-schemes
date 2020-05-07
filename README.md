# 中州韻粵語拼音輸入法分歧拼音系統補丁
* 依賴於：[`rime/rime-cantonese`](https://github.com/rime/rime-cantonese)
* 呢個補丁將`jyut6ping3*.dict.yaml`嘅詞句轉換成其他主流拼音系統，方便唔係用開「粵拼」嘅人用RIME，同埋學習用「粵拼」轉寫。
* 本方案唔係rime-cantonese嘅分歧拼音系統方案，而只係一個幫助大家學習「粵拼」嘅教育工具。所以使用哩個補丁嘅時候係會預設顯示該詞嘅正確粵拼，而唔係分歧系統之下嘅拼音。
* **長遠請考慮轉用香港語言學學會嘅粵語拼音方案（「粵拼」），一嚟科學，二嚟貼近國際音標，三嚟大部分嘅現代粵語資源都係用「粵拼」標音。如果閣下希望同本地粵語文化接軌，請轉用粵拼。**
* 呢度嘅程式碼係都以補丁方式實現，唔會影響其他輸入法檔案。

## 我用緊邊種拼音系統？
拼音系統  | 「翠」| 「獎」 | 「完」 | 「花」 | 常見於（純粹主觀感覺）
 :-------------: | :-------------: | :--------: | :---: |:----: | -----
 [國際音標](https://zh.wikipedia.org/wiki/%E5%9C%8B%E9%9A%9B%E9%9F%B3%E6%A8%99) | t͡sʰɵy | t͡sœːŋ | jyːn | faː | 語言學研究
 [**粵拼**](https://zh.wikipedia.org/zh-hk/%E9%A6%99%E6%B8%AF%E8%AA%9E%E8%A8%80%E5%AD%B8%E5%AD%B8%E6%9C%83%E7%B2%B5%E8%AA%9E%E6%8B%BC%E9%9F%B3%E6%96%B9%E6%A1%88) | **ceoi** | **zoeng** | **jyun**| **faa** |**現代學術資料，社羣粵語資料，字典**
[耶魯拼音](https://zh.wikipedia.org/wiki/%E8%80%B6%E9%AD%AF%E6%8B%BC%E9%9F%B3#%E7%B2%A4%E8%AF%AD%E8%80%B6%E9%B2%81%E6%8B%BC%E9%9F%B3)|  cheui | jeung | yun | fa| 上世紀學術資料，Gboard等輸入法
[教院拼音](https://zh.wikipedia.org/wiki/%E6%95%99%E8%82%B2%E5%AD%B8%E9%99%A2%E6%8B%BC%E9%9F%B3%E6%96%B9%E6%A1%88) | tsoey | dzoeng | jyn | faa| 香港教育局教材
[劉錫祥方案](https://zh.wikipedia.org/wiki/%E5%8A%89%E9%8C%AB%E7%A5%A5%E6%8B%BC%E9%9F%B3)| chui| jeung| yuen | fa| 外國，「網上廣東話輸入法」，面向外國人嘅粵語教材
[黃錫凌方案](https://zh.wikipedia.org/wiki/%E9%BB%83%E9%8C%AB%E5%87%8C%E7%BE%85%E9%A6%AC%E6%8B%BC%E9%9F%B3)|tseue|dzeung|yuen|faa|《粵音韻彙》
[饒秉才方案](https://zh.wikipedia.org/wiki/%E5%B9%BF%E5%B7%9E%E8%AF%9D%E6%8B%BC%E9%9F%B3%E6%96%B9%E6%A1%88)|cêu|zêng|yun|fa|大陸部分著作

## 點解我要學粵拼？

序：以下我哋會解釋比您聽點解您我哋嘅輸入化方案係用「粵拼」嚟設計，同埋點解您 **應該停用分歧拼音系統，轉用「粵拼」**。

### 拼音方案設計原則

拼音方案又叫羅馬化方案。因爲漢字唔係表音文字，所以用漢字書寫嘅語言都需要一個拼音方案嚟表達佢嘅發音系統。所以對於拼音方案嚟講，最重要嘅用途就係清晰準確噉表達到呢門語言嘅音位系統。當然喺廿一世紀計算機時代，拼音方案又多咗另一個重要用途就係協助計算機信息處理。根據呢兩點，我哋可以總結出一啲評價拼音方案優劣嘅原則。我哋只需要根據呢幾條原則，就可以評判一個拼音方案係設計得好定係差。跟住落嚟我哋會逐個講解呢幾條原則，並且分別舉例說明，點解我哋要用粵拼，而唔用其他方案。

#### 原則一：「一個符號對應一個音位」

拼音方案要清晰準確兼簡潔噉表達音位系統，就需要遵循「一個符號對應一個音位」原則。亦即係話，一個拼音方案入邊如果出現咗「一個符號可以代表多個音位」或者「一個音位可以用唔同符號轉寫」，噉我哋就可以話呢個拼音方案係混亂唔一致嘅，無法準確簡潔噉表達呢門語言嘅音位系統。

一個最熟悉嘅反例就係我哋嘅普通話拼音系統（《漢語拼音方案》），佢入邊 j q x 呢三個符號，同埋 g k h 呢三個符號，當後面接嘅韻母係 i 個陣，佢哋代表嘅其實都係相同嘅三個音位 /k/ /kʰ/ /h/。佢設計成 j q x 係爲咗轉寫佢嘅實際音值 [t͡ɕ] [t͡ɕʰ] [ɕ]。所以呢度就出現咗「同一個音位用唔同符號轉寫」嘅現象，係一個設計缺陷。正確嘅做法應該係用返 gi ki hi 嚟表示現有嘅 ji ci xi 三個音。

呢一個原則仲有另一層意思，就係一個符號具體表達嘅發音，唔應該依賴佢嘅環境（即係旁邊嘅符號）。咩意思呢？我哋以耶魯粵語拼音爲例。耶魯拼音入邊，字母 a 既可以表示長 a，又可以表示短 a。下邊嘅表格表示咗耶魯拼音對三隻字「花」「翻」「分」嘅拼法。我哋可以睇到佢喺開音節（冇鼻音或者入聲韻尾）個陣 a 代表 /a/，閉音節（有鼻音或者入聲韻尾）個陣代表 /ɐ/，呢個就係「一個符號 a 代表 /a/ 同 /ɐ/兩個音位」。同樣嘅，「花」同「翻」嘅韻母係一樣嘅，但係佢一個拼成 fa 一個拼成 faan，即係「一個 /a/ 音位用 a 同 aa 兩個符號嚟表示」。

**表一：耶魯拼音嘅/aː/同埋/ɐ/**
| 花 /aː/ | 翻 /aː/ | 分 /ɐ/ |
| ------ | ------ | ------ |
| fa     | faan   | fan    |

所以耶魯呢度就係「依賴環境嚟確定一個符號實際代表咩音」，符號 a 究竟代表 /a/ 定係 /ɐ/ 要靠係開音節定閉音節嚟判斷。呢個就係耶魯設計得唔好嘅地方之一。**粵拼統一規定 aa 就係 /a/，a 就係 /ɐ/ 唔需要依賴環境一睇就明。**

#### 原則二：避免使用附加符號同非 ASCII 字符

呢一條原則，係出於計算機時代方便信息處理考慮嘅。我哋要儘量令一套拼音方案僅使用 ASCII 字符集（美國資訊交換標準代碼）入邊嘅字符，噉樣可以避免好多潛在嘅問題同麻煩。換句話講，我哋要儘量使用廿六個英文字母加數字就表達晒成個拼音方案，而且唔好用 ´ˋˇ˘˜ 呢啲符號。

一個最熟悉嘅例子，就係普通話拼音方案入邊嘅 ü。相信大家都清楚打呢個 ü 有幾麻煩，估計大家平時打呢個符號都係網上複製粘貼落嚟嘅。用 ü 呢個符號除咗輸入麻煩之外，仲有個問題就係佢唔係 ASCII 字符集入邊嘅字符，所以冇辦法用最簡方式嚟編碼（轉成 v 係另一回事），噉樣喺編碼轉換個陣就有可能出意想不到嘅 bug。同樣嘅，普通話拼音用 ˉˊˇˋ 四個符號嚟標註聲調，輸入唔方便亦都容易出錯。當然呢個係因爲普通話拼音方案喺上世紀五十年代設計，嗰陣計算機仲未普及，所以呢處疏忽都係正常嘅。

另一方面，我哋知道拼音方案仲有一個用途就係攞嚟做拼音輸入法。如果一個拼音方案到處都係 ˉˊˇˋ，大家又點打字呢？好彩普通話拼音入邊呢啲符號凈係用嚟表示聲調，而普通話拼音輸入法就算唔打聲調都係冇問題嘅。如果話呢啲符號唔單只用嚟表示聲調，仲要攞嚟區分輔音元音，好似 ü ö ä 噉嘅話就大鑊嘞，拼音輸入法可能會麻煩到大家都唔想用。**粵拼正正只用鍵盤上有嘅英數字嚟表音，唔使執字粒噉麻煩。**

#### 原則三：符號選擇儘量符合大衆習慣

呢條原則嘅意思係，選擇字母嚟對應發音個陣，要儘量符合大家嘅既有認知，例如字母 a o e 一般用嚟表示元音、b p m f 表示脣音等等。一個比較出名嘅反例就係切洛基語嘅書寫系統，佢用字母 Ꭰ 嚟表示發音 /a/，字母 Ꮃ 表示發音 /la/，呢個就比較反直覺嘞。再例如話普通話拼音嘅 q 代表發音 /t͡ɕʰ/，呢個就唔符合英語人士嘅習慣，因爲英文入邊 q 一般表達 /k/，所以西方人學普通話拼音第一次睇到呢個 q 個陣，就容易下意識噉發成個 /k/ 音。

粵拼經常畀人批評用字母 j 嚟表示個發音 /j/，就係因爲違背咗呢條原則，因爲大家都習慣咗用字母 y 嚟代表個發音 /j/，用 j 嚟表示就好唔習慣。關於呢一點 [下面](README.me#粵拼嘅缺陷) 會詳細解釋。

#### 原則四：準確反映語言音位系統

呢條可以講係最重要嘅設計原則，但亦都係最麻煩最容易出問題嘅。因爲音位分析有一定嘅主觀性，有時無法將一門語言嘅音位系統完全確定落嚟。最典型嘅例子就係普通話，目前學術界對語普通話嘅元音音位數量仲未有一致共識（例如是否考慮埋兒化音又會影響個分析結果）。所以呢啲差異都會直接影響到拼音方案嘅設計，有時甚至會影響到拼音方案嘅表達能力，導致個方案冇辦法表達一啲音，呢個就屬於設計失誤嘞。關於呢一點我哋下面會舉例說明。

### 其他粵語拼音方案嘅缺陷

明白咗拼音方案嘅設計原則之後，我哋就可以嚟逐個睇，點解話粵拼係設計得最好嘅粵語拼音方案，其他唔得。我哋跟住落嚟將四個最出名嘅粵語拼音方案：耶魯拼音、教育學院拼音方案（教院式）、廣州話拼音方案（饒秉才），講下佢哋點解設計唔好，從而證明點解我哋要揀粵拼。

#### 耶魯拼音

耶魯拼音算係除咗粵拼之外，最常見嘅粵語拼音方案嘞。同粵拼相比，佢主要有下面幾個區別：

1. 耶魯拼音中，/a/ 喺開音節用 a 表示，閉音節用 aa。/ɐ/ 喺閉音節中用 a 表示，無法表示開音節 /ɐ/。
2. 耶魯拼音用 j ch y 嚟代表 /ts/、/tsʰ/、/j/ 三個音。因此元音 /yː/ 需要用 yu 嚟表示。
3. 耶魯方案唔區分 /ɵ/ 同埋 /œ/，兩者都用 eu 嚟表示。亦都因爲噉耶魯拼音無法表示 /ɛːu/ 呢個音。
4. 耶魯用附加符號 ˉˊ 同埋字母 h 嚟表示聲調。

我哋而家逐個嚟睇，呢幾條設計究竟有乜問題。首先第一點我哋喺上文嘅原則一中已經講過。耶魯拼音噉樣設計，係因爲當年嘅音位分析認爲開音節 /ɐ/ 並唔存在，所以乾脆將開音節 aa 都縮寫成 a。噉一縮寫法個問題就大嘞，首先佢違背咗我哋嘅第一條原則「一個符號嚴格對應一個音位」，令學習者困惑，增加粵語學習者嘅學習成本。然後佢噉導致無法表達開音節嘅 /ɐ/ 字，例如語氣詞「嘞」，違背咗原則四。所以呢一點係耶魯拼音好大嘅設計缺陷。

第二條入邊，耶魯拼音用咗 yu 嚟表示 /yː/，又係違背咗第一條「一個符號對應一個音位」嘅原則，因爲佢需要根據佢嘅環境嚟判斷實際發乜音。。因爲耶魯拼音已經用咗 y 嚟代表 /j/、u 代表 /u/，而家又規定 yu 組合起身變成 /yː/，即係「一隻字母代表一個單元音，組合起身又代表另一個單元音」，噉樣一嚟又係令學習者困惑，二嚟都唔方便計算機信息處理（輸入法難以處理簡拼、寫正則表達式都要加入環境判斷）。呢個又係一個設計缺陷。關於呢一點，喺最尾嘅[粵拼缺陷](#粵拼嘅缺陷)我哋會再做進一步說明。

第三條，耶魯拼音用 eu 嚟代表 /ɵ/ 同 /œ/，呢個就係原則四入邊講嘅音位分析嘅問題嘞。呢條直接導致咗耶魯拼音冇辦法表示 /œ/ 同 /ɛːu/ 呢啲音，影響咗呢個拼音方案嘅表達能力。

**表二：耶魯拼音嘅/ɵi/，/ɛːu/，/œt/**
|          | 睡 /sɵi˨/ | 掉 /tɛːu˨/ | 𠰲 /œt˨/ |
| -------- | --------- | ---------- | -------- |
| 耶魯拼音 | seuih     | 無法表示   | 無法表示 |
| 粵拼     | seoi6     | deu6       | oet6     |

第四條用附加符號同埋 h 嚟表示聲調，例如「蛇」嘅發音拼成 sèh，呢點就可以講比較怪異嘞。佢既違背咗原則二，又違背咗原則一，因爲 h 已經用咗嚟表示聲母 /h/。好彩新版耶魯拼音都增加咗用數字嚟表示聲調嘅方案，噉樣對於信息處理係個好大嘅幫助。

所以綜合嚟講，耶魯拼音嘅設計違背咗原則一二四（第三條比較主觀好難判斷），呢啲設計缺陷足以令我哋放棄耶魯拼音改用粵拼。

#### 廣州話拼音方案 (饒秉才方案)

廣州話拼音方案係 1960 年廣東省政府公佈嘅粵語拼音方案，後嚟喺 1980 年出咗修訂版，因爲係饒秉才教授修訂嘅，所以又稱饒秉才方案。我哋呢度以 1980 年修訂後嘅版本爲準，講解呢個方案有乜設計問題。廣州話拼音方案同粵拼嘅主要區別有以下：

1. 用 e ê é ü 分別表示元音 /ɐ/、/œː/、/ɛː/、/yː/
2. 用 y 表示輔音 /j/，gu、ku 表示 /kʷ/、/kʷʰ/
3. 同時用 z c s 同 j q x 嚟表示 /ts/、/tsʰ/、/s/，兩組其實冇分別，都係表達同一組音位
4. 入聲韻尾用 -b -d -g 表示
5. 唔區分 /ɵ/ 同 /œ/，無法表示

呢度就可以睇得好清楚嘞，第一點可以講係完全違背晒原則二，用咗大量嘅附加符號嚟表示啲元音。呢個嚴重阻礙咗電腦信息嘅處理，亦都冇辦法用嚟做輸入法。而第三條就顯然違背咗原則一，同一個音位用唔同嘅符號嚟表示。呢條設計係爲咗兼容普通話拼音，但其實係完全冇必要嘅，反而仲增加咗困惑度。

而第二同第四點都係比較主觀嘅符號選擇問題，唔可以算缺點，第五條就同前面講嘅耶魯拼音一樣。所以總嘅嚟講第一同第三點係最嚴重嘅缺陷，呢兩點直接決定咗呢個拼音方案冇辦法喺信息時代推廣普及。

#### 教院式拼音
（待擴充）

### 粵拼嘅缺陷

粵拼畀人批評得最多嘅，就係個 j 嘅問題嘞。好多人都問點解唔攞 y 嚟表示 /j/，因爲呢個的確符合大衆嘅習慣，無論係普通話拼音定係英文都係用 y 嚟表示 /j/。噉點解粵拼要違背原則三用 j 嚟代表 /j/，而唔用 y 呢？因爲如果我哋用咗 y 嚟表達 /j/，噉會引申出一個問題：廿六個英文字母就得咁多，家陣用咗 y 嚟表示 /j/，噉我哋用乜嚟表示 /y/？

對於呢個問題，耶魯拼音嘅答案係：用 y 表示 /j/，然後用環境判斷咩時候代表 /y/。如果字母 y 後面跟嘅係 u，噉兩個字母串起身就代表 /yu/。呢個亦即係上文講到嘅「一隻字母代表一個單元音，組合起身又代表另一個單元音」。即係話，**耶魯拼音犧牲咗原則一嚟換取原則三**。呢個就係取捨嘅問題嘞。噉邊個原則重要啲？好明顯係第一個，「一個符號對應一個音位」重要啲。因爲呢個一一對應關係如果打破咗嘅話，會帶嚟好多麻煩，上文都講過嘞。而且用 j 嚟代表 /j/，都唔係咩太違背原則三嘅選擇，因爲嚴格嚟講用 y 嚟代表 /j/ 只不過係普通話拼音同英文嘅書寫習慣。世界上仲有好多語言，例如德文就係用 j 嚟代表 /j/ 嘅。所以換句話講，只不過係普通話拼音同英文使用者覺得粵拼噉設計唔適應，換成德文使用者就會覺得好自然嘞。況且大家都睇到，國際音標入邊呢個音（硬齶近音）嘅符號就係 /j/，所以粵拼噉寫只不過係遵循國際音標噉解。

如果真係話粵拼有咩大嘅設計缺陷嘅話，噉的確有一個，就係用兩個字母 yu 嚟表示元音 /y/，顯得冗長冇必要，因爲完全單用一個 y 就搞掂，而且冇副作用。LSHK 當初設計噉用兩個字母，係考慮到大衆習慣同歷史遺留問題（原則三）。不過好消息係，目前大部分粵拼輸入法都支持 y = yu 嘅縮寫，所以大家打字嗰陣如果懶得打 yu 兩個字母，單打一個 y 都係完全冇問題嘅。

>劉邦後代（2020）。《點解要用粵拼，唔用其他粵語拼音方案？》。*jyutping.org*。（網絡連結：https://www.jyutping.org/blog/scheme/ ）

上文已徵得作者同意，轉載於此，以求一正各粵語拼音系統羣立之亂象，奠立傳承粵語文化之基礎。

## TL;DR

|                  準則| 粵拼  | 耶魯 | 教院  | 饒秉才|
| ------------------- | ----- | -----| -----| -----|
| 一個符號對應一個音位  |  ✓    | ✗   |  ✗    |  ✓   |
| 只用鍵盤打得出嘅英數字|  ✓    | ✗(聲調)| ✓  | ✗ |
| 符號符合大衆讀音     | ✓     | ✓    |  ✓   | ✗ |
| 反映IPA音位         |   ✓   | ✗    |  ✓   | ✗ |  

### 所以...

如果睇完以上嘅簡介，閣下已經決定咗要學習「粵拼」，但係覺得無從入手，噉喺[呢度](INSTRUCTIONS.md#安裝方法)我提供咗幾個過渡方案，俾閣下用住熟悉嘅拼音嚟用RIME先。選字表上面會顯示正確嘅粵拼，方便大家對照讀音。

如果係學習上遇到啲咩嘢困難，歡迎加入我哋嘅[Telegram羣組](https://t.me/rime_cantonese)，入面有大量嘅粵拼專家，「唔識教到你識」爲止。

當你對自己嘅粵拼有信心嘅時候，就可以參考[呢度](INSTRUCTIONS.md#解安裝方法)嘅方法，將補丁移除，體驗中州韻輸入法嘅完整功能。

## 授權條款
GNU較寬鬆公共授權條款（第三版）。詳細條款請參閱[LICENSE](LICENSE)。
