# Git 極簡介

- 因為從本機建立目錄上傳有點技術上的問題，建議倒過來做：
   1. 在GitHub上建立一個專題；
   2. 將你本機上的檔案上傳至目錄中。
   3. 再用 git clone 專題的網址 將專題下載到你想要的本機目錄之下。
   4. 然後，你就可以在本機做下面動作了：
- 以下都在終端機進行：
   5. 前進到那個目錄，鍵入：git init，將該目錄設成git儲存庫(repository)。
   6. 鍵入 git config --global user.name "GitHub名字"
   7. 或是，鍵入 git config --global user.email "GitHub email"
   8. 可以使用 git status 來看看目前你的儲存庫的狀態。
   9. git add 檔名 或是 . => 把某個檔案或是儲存庫中所有檔案(用黑點的話)加入要做處理的幕前。
   10. git commit -m "訊息" => 「訊息」是簡要記錄這個板本的變更，用commit讓Git記錄此次的變更。
   11. git diff 還原點編號1 還原點編號2 => 比較兩個還原點編號的差別（不同的行會標出來）
   12. git checkout 還原點編號 => 回到這個編號的內容，捨棄其後的變動。檔案內容會立刻改變。
   13. 還原後，還是要做：git add . 以及 git commit -m "訊息"，以記錄變動。
   14. 使用 git push -u origin main 將修改後的檔案上傳至GitHub中
- 要建立 SSH：
   1. MacBook：
      ``` 
      ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
      (按enter，一直到輸入密碼；密碼要記下來，常用到)
      eval "$(ssh-agent -s)"
      ssh-add -K ~/.ssh/id_rsa
      cat ~/.ssh/id_rsa.pub
      (接下來會出現一大串的SSH Key，複制下來；
      進到GitHub你的帳號下的設定，選擇SSH及GPG keys，
      將其複制儲存即可。)
      ```
   2. Windows: https://blog.alantsai.net/posts/2015/09/use-ssh-in-windows-for-github