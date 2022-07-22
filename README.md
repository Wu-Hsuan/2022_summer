While I learn in Droidtown
# 2022/07/01
## 斷詞歷史
- mmseg： 維護字典，長詞問題，選長的，但會永遠處理不完
    - jieba，根據特定領域文本作語料庫，
        - 簡體版本，人民日報
        - 繁中版本，有新詞問題，加/不加都不好

- 統計方法： 前後兩個字一起出現的比例，機率高，一起的，一樣需要根據特定語料庫計算，分布，跟誰放在一起

- CKIP, classical，原理與結巴一樣，看多個字再一起出現的比例，有新詞未更新問題。(號稱96% ↑ 的正確率)
    - tagger, bert
    - light verb/輕動詞：感覺像動詞、導致什麼發生，有什麼事發生了。e.g. this movie [makes] (使) me happy. 我是[搞]飛機的。 幫你[用]到好。
   

    - insight: 人看到第一次見的例子，不會看不懂，but ml can't。大腦運作的方式或許不同。
        - e.g.用電鰻的電電電鰻電鰻會被電鰻的電電死嗎。
        - 特定字元，pattern，始能理解某一處的作用。
        - 機器也需要學會，讀的方法，讀文章的方法，讀表格的方法。
        - 基於架構/結構，or基於data。
        - 分辨先天與後天，語境是後天需要學習的，e.g.你再做一次試試看。
        - 
        - 

- spacy框架->nltk

- monpa-> 學ckip，150個char訓練效率最佳，速度快。北醫，運用在病歷上(不會寫太長)。

- hanLP 一個框架，可load不同model，調整之前的模型

# 2022/07/08
## AI的三次revolution：
1. 類人腦(1954s)：語言學家分成corpus linguistics、computational liguistics(performance) ∕ Chompsky的formalism(形式語言學_X-bar)
2. 專家系統(80~90s)：做某種特定的任務
3. Big Data、Machine Learning(2012、2013s)

- BD革命(？)顯卡 ： ATI(nVidia) → AMD
- X-bar：minimalist program
- overfitting(過擬和)：錯誤及正確的都學習

## CKIP
    - 可能是用正確答案trainning(SIGHAN2005：gold standard)：400句錯誤都一樣
    - OOV(Out Of Vocabulary)(字典外的字)
      - e.g.被「陽」了 → 如果這句話存活很久，可能被X結構或陽當動詞流行
    - CWs：97.49% / POS： 94.59% / NER： 77.98% → NLP App相乘 = CWS*POS*NER = 72.21%
     
## Liciensing
      - GPL：需要一樣授權，且用了就需要公開(自由下載)，For 學術、銀行(病毒性、有感染力的授權)
      - MIT：不管是否公開，但是授權系統需要在同樣授權的系統中運作
      - Appache：是否公開可以分開
      - Open CC(CC0)：0保障0責任0限制
 
## Articut
 - ENTITY_OOV∕ENTITY_nouny∕ENTITY_nounhead
 - NER∕POS
 - TF-IDF(Term frequency - Inverse Document freq.)
    -key word 最有區辨性∕代表性的字(not關鍵字)
 - text → NER/POS → TF-IDF 
   v.s. text → jieba/CKIP → TF-IDF(去stop word 停用詞)(英文的function word)
 
## 給權重的方法(0714 by Peter)
1. 我隨便給的 (那你誰啊？)
2. 我依資料分佈給的 (那資料哪來的？)
3. 我依抽樣結果給的 (那你怎麼抽的？)
4. 我擲筊得來…(擲 1 次是迷信、3 次是運氣、100 次是為了抽汽車、1 億次就叫大數據了)
5. 我抄別人論文裡的參數 (哪一篇？它在幹嘛？請報告說明一下。) 
 
 
# 2022/07/15
##  檢討作業：
    1. 廣告or社交e-mail:
        - 建ADs、社交和其他的名詞和動詞建立corpus
        - 將社交郵件跟ADs郵件重疊的動詞跟名詞去掉
        - 將與其有來往的帳號設定為社交郵件
    2. 詐騙or廣告&其他簡訊
        - term、word不足
        
Context：語境

## NLU
1. Eliza
2. LUIS
    - 一個一個字學習
3. GoogleDialogFlow

二兆三星
中央資工蔡宗翰教授：Hybrid → ML、DL (有錢惹！)
(台語斷詞)
專利：依照標點符號中文斷句
    
4. Wolfram Alpha：https://www.wolframalpha.com/
5. Knowledge Graph 廣義知網：https://ckip.iis.sinica.edu.tw/project/ehownet
    - 專家寫規則，分類什麼和什麼有關
    - inconviente：要不斷有人維護
    - Ontology(本體論)

ref檔：分享用檔案


# 2022/07/22

## Loki v.s. Machine Learning
### 聊天機器人
    1. clickbot
    2. 關鍵字
    3. 純機器學習
        - 天氣預報
        - 容易預測錯誤 e.g. 問路結果幫你叫車
        - IBM的Watson → 資料量不夠大，有六分之五的資料是抹你出來的假資料
            醫療聊天機器人無法解釋成因，且建議處方舊
        - 國泰的「阿發」(關鍵字？) v.s. 小玉(ML+LOKI)
    4. 句型結構比對式
        - 句型是有上限的 e.g.便利商店
    
## 不同意圖的同樣句型是否會造成混淆？
    1. 分類不同意圖的project
    2. 有些不同的utterance可以互通
    3. 以LOKI為例，可以分別選擇要勾選的替換詞類
    4. 應用：電商平台的推薦系統
    
## NLU with sympy math (Pycon 2022)
    1. semantics = entity + relationship
    2. 把所有問題都當成alignment problem
    
## Example
    1. 人力銀行不能標註派駐大陸，如何篩選出派駐大陸的職缺
        - DICT
        - google map
    2. 書店店員 chatbot
        - function：bargain、price、membership、bookshelf、availiability、report problem
        - 可配合情緒分析(keymoji)
        - chatbot有機會與不同情境結合 e.g. 民宿
        - 不同的 chatbot 最好只做一件事，不然很有機會犯錯
         → intent可以儲存
    3. 知識運算
        - 爸爸帶回來一隻小狗，我們給這隻小狗吃洋芋片。
            -小狗可以吃洋芋片
 

    
RE是什麼？
