## 測試環境建置
- 以ubuntu 20.04/18.04 LTS或Kali linux
- [安裝peda](https://github.com/longld/peda) 
```
git clone https://github.com/longld/peda.git ~/peda
echo "source ~/peda/peda.py" >> ~/.gdbinit
```
- [GHidra](https://ghidra-sre.org/)
- [pwntools](https://ithelp.ithome.com.tw/articles/10227326)
```
sudo apt install python-pip
sudo pip install pwntools
```


## 第一題:Buffer overflow-1

- 1-1.pass [上課示範解題]
- 2-1.張元_Pwn-1 

## 第二題:Buffer overflow-2==>ret2code

- 1-2.gohome [上課示範解題]
- 1-3.registration 
- 1-10.Angelboy_Pwn-1 
- 1-9.張元_Pwn-8 

## 第三題:Buffer overflow-3==>ret2sc shell code
- level-1.Angelboy_Pwn-2 [上課示範解題]
- level-2.張元_Pwn-9



# 【解題說明】建議事項

- 程式行為分析
  - file 《binary》
  - strings 《binary》
  - pwn checksec《binary》或使用gdb-peda的checksec
  - 執行時的輸出與輸入

- 逆向分析
  - static analysis  ==> radare2, ghidra,...
  - dynamic analysis ==> gdb-peda, ...  

- 撰寫exploit code
  -  清楚說明exploit 的邏輯
  
