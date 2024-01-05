# HW1-1
● 可藉由 input()輸入一個 1 到 20 的數字 n，如下圖。若輸入格式有誤， 或非在 1 到 20 之間，都應跳出錯誤訊息，要求重新輸入。譬如輸入-2, 3.4, aa, -7 或是 21, 35 都將視為輸入錯誤。 

![image](https://github.com/cindy-lai0202/Introduction-to-ML/assets/72913466/99cfe309-60c6-4003-991f-915993ca06bf)

● 之後依據數入數字 n 從放置於目錄./test 下之檔案 picn.jpg 的圖片顯示於螢幕上。譬如：若輸入 15，則 pic15.jpg 將顯示於螢幕，如下： 

![image](https://github.com/cindy-lai0202/Introduction-to-ML/assets/72913466/e14a22b7-9708-4353-9ced-f29a54d44135)

 ./reference 目錄下的子目錄 cats/及 dogs/已分別收錄 50 張貓及狗的圖片。請從這 100 張圖片中，找出最接近所選擇圖片之 3 張圖片，並將結果顯示於螢幕上。判斷兩張圖片相似度的指標可以採用底下公式：
 
 ![image](https://github.com/cindy-lai0202/Introduction-to-ML/assets/72913466/0025328e-2715-4947-ac9a-aebeef7412b3)

  ● 請依此判斷該圖片應為狗或者是貓。 
  ● 也請於 jupyter notebook 上面討論，此一判斷所選擇之圖片是貓還是狗的方式可能的問題。


# HW1-2
說明:撰寫一個 python 程式利用 pandas 讀取 HW1_data.csv 資料:

● 計算出 Age, HR, Height, Weight 及 BP 的平均值加於 dataframe 最下列。（請注意避免累加過程中出現 overflow 現象） 
● 利用程式找出並於螢幕列出各分項指標 feature（Age, HR, Height,  Weight 及 BP）中之最大者的姓名（Name）。 
● 請繪製身高體重（Height, Weigth）之散佈圖（Scatter Plot），女生請以 紅點標示，男生請以藍點標示。 
● 繪製不同年齡（Age）區間的人數直方圖及圓餅圖（Pie Chart）。請依 1-10, 11-20, 21-30…每 10 歲為一個區間統計。 
● 繪製男女性別分佈比例之圓餅圖（Pie Chart）。 


# HW2
使用 regression 預測房價(SalePrice)。
1. 讀入資料,並判斷出那些數據格式不是數字,或是有缺失值。
2. 將非數字類型的資料進行編碼。請比較至少兩種的編碼方式,比較其效果。
3. 填補缺失值。
4. 將資料切割成訓練集 70%,預測集 30%。分別使用 Linear、Ridge、及 Lasso 三種 regression 模型預測 Rating,並使用 MSE
(Mean-Squared-Error)作為預測準確度的指標。比較那一種模型較佳。
5. 依據最佳結果的模型,對預測集資料繪製出預測房價 vs 實際房價之散佈(scatter plot)圖
6. 比較將特徵值進行標準化前處理後之預測準確度
7. 利用相關係數選取特徵使用:利用 pandas 套件中 dataframe 之函數 corr()找出各特徵之間的相關係數,並利用 seaborn 套件之
  heatmap()函數繪製。
● 僅使用與房價最相關的前四高係數之特徵進行預測
● 僅使用與房價最相關的前四低係數之特徵進行預測
● 比較使用前四高、前四低及所有特徵三種狀況所得到預測準確度的差異
8. 利用 matplotlib 套件繪製特徵 GrLivArea 與房價 SalePrice 之散佈(scatter plot)圖,判斷是否有極端之 outliners,請將
   之移除後再比較預測準備度。


# HW3-1
針對員工離職率(left)進行預測
1. 讀入資料,並判斷出那些數據格式不是數字,或是有缺失值。
2. 將非數字類型的資料進行必要的編碼。
3. 若有缺失值請填補。
4. 將資料切割成訓練集 70%,預測集 30%。
5. 利用 Logistic Regression 模型進行預測。
6. 請針對各個特徵與離職率的關係進行探討。看是否透過特徵轉換提高預測之準確率。



# HW3-2
使用 Linear Regression 預測在不同的時間,租借共享單車的人數預測(count)
1. 讀入資料。
2. 對日期欄位進行處理。
3. 利用 regression 推測使用人數。顯示出預測結果。


# HW4-1
針對員工離職率(left)進行預測
1. 讀入資料,並判斷出那些數據格式不是數字,或是有缺失值。
2. 將非數字類型的資料進行必要的編碼。
3. 若有缺失值請填補。
4. 將資料切割成訓練集 70%,預測集 30%。
5. 利用 Decision tree 及神經網路模型進行預測。
6. 請與前次 Logistic Regression 的預測準確率進行比較。請探討那個模型比較適合,其可能原因為何?


# HW4-2
針對信用卡交易資料,預測是否為詐騙的交易(class==1)
1. 讀入資料、切割資料(測試集佔 30%,訓練集佔 70%)
2. 利用 Decision tree 及神經網路模型進行預測,計算出 Accuracy,Recall, Precision, F1-Score。
3. 統計 class==0 及 class==1 的資料比數,看是否類別間資料數量是否有很不平衡的現象。
4. 為了要提高 recall 的數值,請:
● 改變 Decision tree 及神經網路模型中類別權重或訓練權重,計算新的結果,與之前結果比較。
● 利用 imbalanced-learn 套件中 SMOTE 的方法來增量資料,計算新的結果,與之前結果比較。


# HW5
撰寫捲積神經網路 CNN 對非洲象及亞洲象圖片進行分類。
1. 附件壓縮檔解壓縮後,train/資料夾含非洲象資料夾 African/及亞洲象資料夾 Asian/圖片。請開發捲積神經網路 CNN 能辨識這兩類
圖片。
2. 訓練圖片的解析度不同,請做適當 resize 將其調成一致。
3. 訓練結果請輸出混肴矩陣(confusion matrix),並計算 AUROC 的數值。
4. 程式碼中請將訓練結果利用 model.save_weights()將訓練後的權重存成 elephant.h5 的權重檔。
5. 程式碼請利用 model.load_weights()載入 elephant.h5 的權重,並針對 test/資料夾下的圖片進行預測,並輸出 elephant.csv,其
  格式如下,若預測結果為非洲象填 1, 亞洲象則填 0

![image](https://github.com/cindy-lai0202/Introduction-to-ML/assets/72913466/9a3c1008-9e7e-4169-918b-faf44ad30207)



