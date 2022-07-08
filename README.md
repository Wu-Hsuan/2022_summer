# 2022/07/01
While I learn in Droidtown
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
   - Liciensing
      - GPL：需要一樣授權，且用了就需要公開(自由下載)，For 學術、銀行(病毒性、有感染力的授權)
      - MIT：不管是否公開，但是授權系統需要在同樣授權的系統中運作
      - Appache：是否公開可以分開
      - Open CC(CC0)：0保障0責任0限制
 
- Articut
 - ENTITY_OOV
 - ENTITY_nouny
 - ENTITY_nounhead
