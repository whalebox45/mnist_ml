這是一個用 PyTorch 寫的 MNIST 手寫數字辨識，沒什麼特別的，就是基本的 CNN。 裡面順便寫了一段可以丟自己畫的圖進去預測的邏輯。

怎麼跑
啟動你的 Jupyter 或直接跑 .ipynb。

確定你有裝 torch, torchvision, matplotlib, Pillow 之類的。

執行全部。

關於硬體
如果你用 Mac，裡面預設會去抓 mps。

如果你用 PC，請自己把 USE_MPS 改成 False 讓它去抓 cuda。

模型重點
兩層 Conv2d + 一層 Linear。

沒什麼創意的 ReLU 和 Dropout。

大概跑 15 個 Epoch 準確度就差不多了。

丟自己的圖
找個地方存成 5.1.png（或者你自己改檔名）。

程式會幫你轉灰階、反轉顏色。

內建一個簡易的 Crop 功能，但預設是關掉的（IS_CROP = False），要是預測不準再自己打開。

儲存/讀取
會生出一個 mnist_cnn.pth。

載入模型的部分預設是關著的（LOAD_MODEL = False），想用的話記得手動轉 True。