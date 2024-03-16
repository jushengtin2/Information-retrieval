電影檢索系統MOVIE SEARCH SYSTEM   

簡介-
本研究旨在探討傳統電影搜尋機制的局限性，使用 Boolean retrieval 方法比對電影 metadata，並引入影評資料以個人化搜尋及排序。研究利用 TF-IDF、Word2Vec 和 Doc2Vec 三種資訊檢索模型，比較它們在電影搜尋精準度上的表現。
關鍵字—檢索系統, TF-IDF, Word2Vec, Doc2Vec, 

介紹-
本研究旨在優化電影搜尋機制，挑戰傳統的 Boolean retrieval 方法。傳統機制常僅利用 metadata 比對，無法滿足對電影劇情特色的細緻需求。為此，我們聚焦於結合影評資料和機器學習演算法，提供更個人化且精確的電影搜尋體驗。
過去的研究主要著重在影評的應用，結合 learn to rank、協同過濾等演算法，以實現更智能的電影推薦系統。然而，本研究更進一步探討了 TF-IDF、Word2Vec 和 Doc2Vec 三種資訊檢索模型的應用。這些模型分別基於詞頻、詞嵌入和文件向量化，用以提高搜尋的精確性。
我們選擇使用 IMDB 提供的前 1000 筆評分最高電影資料集，包含導演、演員、電影種類等 metadata，以及電影名稱和大綱。研究假設使用者主要透過電影大綱和名稱進行搜尋。
研究方法包括資料前處理，使用 Python 實現 PorterStemmer、tokenization 和 stopwords removal。隨後，我們分別採用 TF-IDF、Word2Vec 和 Doc2Vec 作為資訊檢索模型，觀察其對搜尋結果的影響。
實驗結果顯示 Doc2Vec 在查詢精確性上表現最佳，而透過調整 Word2Vec 和 Doc2Vec 模型的 hyperparameter，我們進一步提升了模型的性能。總體而言，本研究為電影搜尋系統的優化提供了有益的實證和參考。

資料來源-
本研究的資料來源為 IMDB 上所提供的電影資料集。在這份資料集中，IMDB提供了前 1000 筆評分最高的電影。在這份資料中，包含導演名字、演員名單、電影種類以及電影大綱等資料。在本研究的假設中，我們認為使用者最常使用的方法應當是以劇情關鍵字搜尋電影。因此，本研究決定以電影大綱以及電影名稱作為我們主要的資料來源。
本研究所使用的資料形式如下：
movie title（電影名稱）：
e.g., The Shawshank Redemption
overview（電影大綱）
e.g.,  Two imprisoned men bond over a number of years, finding solace and eventual redemption through acts of common decency.

研究方法-
在本次的研究中，主要使用 python 作為程式語言。在並在使用 PorterStemmer 、 tokenization 以及 stopwords removal 去除無關資訊以得到前處理後資料。
接著，在分別將前處理後資料以三種模型：TF-IDF、Word2Vec以及Doc2Vec 作為資訊檢索模型，並對其提交 query 後的得到回傳結果。隨後，從三種模型的回傳結果中各自取出 5 個相似度最高的答案觀察。

結果－ https://docs.google.com/document/d/1xjVlwt-nqiHmVmC1Kvx_LF_4HFtItZyhKSxqPSyDX_M/edit
各模型平均表現在分別輸入相同的查詢至  TF-IDF、Word2Vec 以及 Doc2Vec 後，人工判定該查詢是否正確，重複數次便能夠得到該模型的平均查詢 precision

