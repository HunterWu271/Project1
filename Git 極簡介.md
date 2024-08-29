# Git 極簡介

1. 首先，在電腦本端建立一個專題目錄。
2. 都在終端機進行：
   1. 前進到那個目錄，鍵入：git init，將該目錄設成git儲存庫(repository)。
   2. 鍵入 git config --global user.name "GitHub名字"
   3. 或是，鍵入 git config --global user.email "GitHub email"
   4. 可以使用 git status 來看看目前你的儲存庫的狀態。
   5. git add 檔名 或是 . => 把某個檔案或是儲存庫中所有檔案(用黑點的話)加入要做處理的幕前。
   6. git commit -m "訊息" => 「訊息」是簡要記錄這個板本的變更，用commit讓Git記錄此次的變更。
   7. git diff 還原點編號1 還原點編號2 => 比較兩個還原點編號的差別（不同的行會標出來）
   8. git checkout 還原點編號 => 回到這個編號的內容，捨棄其後的變動。檔案內容會立刻改變。
   9. 還原後，還是要做：git add . 以及 git commit -m "訊息"，以記錄變動。
   10. TEST
   11. 