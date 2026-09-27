OnlineGDB 的執行與輸入方式：
  執行環境：OnlineGDB (Java)
  輸入格式：請在主控台輸入一行程式碼，例如 ：int result = 7 + 3 + 1 ;
自己選的一組三個數字：
輸入：int result = 8 + 4 + 2 ;
實際輸出的六條指令：
  MOVI R1, 8
  MOVI R2, 4
  ADD R0, R1, R2
  MOVI R2, 2
  ADD R0, R0, R2
  STORE, R0
為什麼第二次可以覆蓋 R2？：
因為執行完 "ADD R0, R1, R2" 之後，前兩個數相加的結果已經寫入到 "R0" 暫存器中。這時 "R2" 原本存放的第二個整數在後續步驟中已經不需要再被讀取，因此可以直接用來存放第三個整數，以節省暫存器資源。
# java-week2-mini3
