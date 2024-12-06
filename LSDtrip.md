![image](https://github.com/user-attachments/assets/a962429d-87f1-426c-8001-ecb17b34836e)

🔗 https://crackmes.one/crackme/673df8399b533b4c22bd2f1b
# WRITE-UP
- Download file về máy, thì ta được file "673df8399b533b4c22bd2f1b".
- Giải nén file "673df8399b533b4c22bd2f1b" và thực thi file "LSDtrip", ta được như sau:
  
   ![image](https://github.com/user-attachments/assets/3275887e-0311-4440-82c9-7c9014042f06)
  
- Nhập password bất kì.
  
  ![image](https://github.com/user-attachments/assets/032a1c54-94a2-41cd-86fb-8c352fe676d0)

- Để có được password thì mình cần dùng ghidra để phân tích file thực thi "LSDtrip".
- Sau khi phân tích file bằng Ghidra, ta thấy tại hàm FUN_00401000 và kết quả khi thực thi file như trên ta thấy có điểm tương đồng nên ta sẽ bắt đầu phân tích ở hàm này.
  
  ![image](https://github.com/user-attachments/assets/7084a227-ae73-4f3e-b69c-1fa5e2f570ab)
  
- Ta thấy password ta nhập vào có độ dài bằng 5 và local_c = 0x3b1 (hex) = 945 (dec).
- Ở đây ta có 2 hướng giải:
- 1. Tìm mật khẩu với độ dài bằng 5 và khiến cho local_c = 945.
  2. Dùng Ghidra và x32dbg để crack file thực thi.
- Sau đây là hướng xử lí theo cách 2.
  
  ![image](https://github.com/user-attachments/assets/0ef6609a-b254-4c04-89b2-745827d50f3e)
  
- Dùng x32dbg để mở file "LSDtrip", rồi dùng "search for >> all module >> string reference" để tìm chuỗi khi nhập đúng password.
  
  ![image](https://github.com/user-attachments/assets/28dd2c9f-7fb2-4977-8a62-fea914e24c3d)
  
- Thay đổi điểm nhảy đến của 004010A3 từ 004010CB thành 004010B8 rồi patch file.
- 
   ![image](https://github.com/user-attachments/assets/40d41013-8b6c-4919-981d-839416f10e22)
  
- Thực thi file vừa mới patch và nhập password bất kì, ở đây ta sẽ nhập "aaaaa" và ta sẽ truy cập được vào file "LSDtrip.exe".

  ![image](https://github.com/user-attachments/assets/428808ea-c136-42f2-84f3-46270ffd37aa)
