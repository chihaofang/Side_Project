此Side Project將針對直播平台之營運目標，從相關利害關係人之角度進行分析，主要分為以下步驟：
1. 定義目標：定義平台希望進行的目標。
2. 具體化目標：將目標聚焦於某個特定事件或行為，以利分析。
3. 根據目標，定義衡量方式與衡量變數。
4. 根據所定義出之變數與衡量方式，進行觀察並分析。

首先，`定義目標`部分為：
* 增加平台使用人數
* 增加平台收入

由於目標通常較為廣泛且能夠切入的角度眾多，以下進行`具體化目標`並限縮範圍：
* 增加直播主的觀眾人數並試著得知觀眾喜歡什麼直播內容
* 分析觀眾何時donate，以此資訊精進直播內容讓願意donate的觀眾能夠付出更多。

備註：以下所稱之使用者與觀眾皆為同一概念。

`定義衡量方式與變數`：根據直播平台三大主要參與者「使用者/觀眾」、「直播主」、「公司」分別以三個notebook進行「以他們的角度出發，該用什麼方式衡量上述具體化目標並且進行分析」。以下將進行三個notebook的摘要：

`User` ： 此notebook從使用者角度出發，討論如何推薦頻道給第一次使用平台的使用者。

作法如下：
* 如果我們能夠得到使用者對於直播主題的偏好，則能根據此偏好搭配直播頻道與直播內容之屬性資料，透過collaborative filtering取出 top-k 相似的使用者，將這些使用者喜歡的頻道推薦給此新使用者。
* 若無法得知使用者偏好，則根據直播內容分類，取各個分類當時熱門的頻道做為推薦。

而已經在使用的使用者，會於`Streamer` notebook討論使用者喜歡此頻道的什麼內容，以此做為促使使用者下次繼續觀看的討論依據。\
會於`Company` notebook討論是否有喜好偏移的現象，以此做推薦頻道的依據。

`Streamer`: 此notebook從直播主出發，
* 先針對直播內容與人氣以及收入，推薦首次直播的直播主，「他可以針對什麼內容，在什麼時間點進行直播」。
* 接著，因為人氣與收入可能會受到「時機點」的影響，舉例：放假與否是否會影響使用者多看或多掏錢給直播主呢? 針對此議題進行分析。
* 最後，針對單一直播主，透過分析直播觀看人數、聊天室留言數、以及donate的金額與時間點，分析「什麼時間點吸引使用者觀看?」以及「什麼時間點吸引使用者付錢?」

`Company` : 此notebook從公司出發，
* 針對推薦頻道的部分，更加細談如何透過使用者操作的過程，逐漸調整推薦的內容直至推薦的內容穩定。
* 針對使用者喜好偏移的部分，從如何判定偏移訊號，一直到最後考量是否要改變推薦內容進行討論。
* 最後，針對donate的部分，分析「直播分類與使用者之下，使用者donate金額與次數」以及「直播分類與直播主之下，使用者donate金額與次數」。

備註：上述notebook的分析使用的資料皆是手動建立，所以可能會與現實上之資料有所出入，但因本side project主要以概念操作為主，所以不影響進行。
