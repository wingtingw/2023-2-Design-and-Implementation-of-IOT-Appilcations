# 2023-spring-Design-and-Implementation-of-IOT-Appilcations

- 組別 : 第三周第五組
- 隊名 : 乖寶寶寶寶乖
- 題目 : 寶寶哭聲偵測

- 組長 :  111550039 張芷翊
- 組員 :  111550120 吳盈庭

- 專題目標：
	- 我們這次實作了一個偵測到寶寶哭了就會傳送即時訊息的裝置，我們結合了NodeMCU板子、IoTtalk平台、以及Linebot三個部分，在NodeMCU板子上我們連接了一個高感度麥克風模組，用來接收寶寶的哭聲，我們會把寶寶的哭聲數據傳到IoTtalk，IoTtalk會連接一個Device Model，我們撰寫程式從Device Model pull 資料下來，並判斷寶寶是不是在哭，若判斷寶寶在哭，就立即傳送Line訊息。我們希望這個裝置可以減少父母親因為沒有注意到寶寶而造成的疏忽，讓寶寶可以得到最即時的照顧，爸爸媽媽也可以及時接收寶寶狀況。

- 程式碼運行方法：
	- 首先須準備一塊NodeMCU板子，並將ArduTalk_ESP12e_1.ino燒錄到板子，然後再設定好網路環境，讓NodeMCU成功連接到IoTtalk平台上。我們的資料夾裡有四個py檔，分別是config.py, csampi.py, DAI.py, DAN.py,使用者須在config.py裡面輸入Linebot的Channel Access Token 和Channel Secret，並更改DAI.py第13行的UserId，接著要運行程式時，須在terminal打python DAI.py的指令。然後上到2.iottalk這台server, 建立專案並新增一個NodeMCU和一個039120_ODF的model, 並各自綁定，這樣就完成了，當偵測到寶寶哭聲，使用者就會收到Linebot傳送來的訊息。

- demo影片：https://youtu.be/t0dYKJ7LpRA?feature=shared
