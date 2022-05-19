## PWN程式漏洞分析與測試報告
```
程式漏洞
程式漏洞資料庫
程式漏洞嚴重度計分系統(Common Vulnerability Scoring System)CVSS
測試環境與工具Pwntools
MYPwnLabA999168測試環境建置
程式漏洞分析實戰1
程式漏洞分析實戰2
程式漏洞分析實戰3
```
## 程式漏洞
## 程式漏洞資料庫
- [CVE](https://cve.mitre.org/)
  - [windows 11 cve](https://www.cvedetails.com/vulnerability-list/vendor_id-26/product_id-102217/version_id-669655/Microsoft-Windows-11--.html) 
- [NVD - NIST](https://nvd.nist.gov/vuln)
- [CVSS程式漏洞嚴重度計分系統](https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator) 


## 測試環境與工具
- 作業系統 建議使用最新ubuntu 2022.04 LTS自建系統
  - [KALi](https://drive.google.com/file/d/1m620Z7KAOSUOLdFH92FYLE2NINb-vJsn/view?usp=sharing) 
  - [陳義賢博士建的Ubuntu 18.04 LTS ](https://drive.google.com/file/d/1aP-qCFP6jKsGYXtKy9ahwZleQSENEi7C/view?usp=sharing)
- [常用工具]
  - [『 Day 26』拜託別 Pwn 我啦！ - 常見的工具 （上）](https://ithelp.ithome.com.tw/articles/10227326) 
  - [『 Day 27』拜託別 Pwn 我啦！ - 常見的工具 （下）](https://ithelp.ithome.com.tw/articles/10227380)
- [Pwntools]
  - [官方文件](https://docs.pwntools.com/en/stable/)
  - [內容豐富的應用解題Nightmare](https://guyinatuxedo.github.io/02-intro_tooling/pwntools/index.html)

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
  
