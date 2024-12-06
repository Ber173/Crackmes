🔗 https://crackmes.one/crackme/673df8399b533b4c22bd2f1b
# WRITE-UP
- Download file về máy, thì ta được file "673df8399b533b4c22bd2f1b".
- giải nén file "673df8399b533b4c22bd2f1b" và thực thi file "LSDtrip", ta được như sau
   ![image](https://github.com/user-attachments/assets/3275887e-0311-4440-82c9-7c9014042f06)
- Để có được password thì mình cần dùng ghidra để phân tích file thực thi "LSDtrip".
- sau khi phân tích file bằng Ghidra, thì tại hàm FUN_00401000 và kết quả khi thực thi file như trên ta thấy có điểm tương đồng nên ta sẽ bắt đầu phân tích ở hàm này.
  ![image](https://github.com/user-attachments/assets/7084a227-ae73-4f3e-b69c-1fa5e2f570ab)
- ảnh trên ta thấy password ta nhập vào có độ dài bằng 5 và local_c = 0x3b1 (hex) = 945 (dec).
  ![image](https://github.com/user-attachments/assets/0ef6609a-b254-4c04-89b2-745827d50f3e)
-
