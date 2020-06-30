# CTF Writeup : Zh3r0 CTF
Author: tg
## 1. Misc
### 1.1 **Welcome to Phase 1**
![welcome](/resource/zh3r0/welcome1.png)
Step 1:
    
    Goto the browser inspact element you will see the flag in the submit button placeholder or you can type manualy.
![welcome](/resource/zh3r0/welcome1_2.png)

#### Flag:zh3r0{is_this_a_real_flag?}

### 1.2 **Welcome to Phase 2**
![welcome](/resource/zh3r0/welcome2.png)
Step 1:

    When we read challange statement you will get hint from there that flag is in zh3ro Discord channel and we have to use man command if we get stuck go and use man command in #shell channel.
![welcome](/resource/zh3r0/welcome2_1.png)
Step 2:
    
    type ls command you will get below data
![welcome](/resource/zh3r0/welcome2_2.png)
Step 3:
    
    Use the command which retrive from man and cat those txt file. BOT will get you a flag.
![welcome](/resource/zh3r0/welcome2_3.png)

 cat welcome.txt so you will get flag go and submit.
![welcome](/resource/zh3r0/welcome2_4.png)
 #### Flag:zh3r0{Hav3_FuN}

## 2. Forensics
### 2.1 **LSB fun**
![welcome](/resource/zh3r0/lsb.png)
Step 1:
    
    Read the statement and you will get the hint that may be flag is in the files LSB (Least Significant Bit).always try guess what kind of method we can apply on the thing.as well as we get the file user.zip unzip it and we get the below image.
![welcome](/resource/zh3r0/lsb2.png)
Step 2:

    Use jsteg that will reveal hidden message and you got a flag go and submit. there are other tools like binwalk,steghide try those also.
![welcome](/resource/zh3r0/lsb3.png)

Tool Source: https://github.com/lukechampine/jsteg
#### Flag: zh3r0{j5t3g_i5_c00l}
## 3. Crypto
### 3.1 **Mix**
![welcome](/resource/zh3r0/mix1.png)
 Step 1:
    Read the statement and you will get the hint. try to fugure out what you can do with the statement and also we got the file with it . so first analysis is that some keyword are CAPITAL and this is a crypto ctf so may be this are the technique used in crypto.download zip extact it and see what can you do with it.
![welcome](/resource/zh3r0/mix2.png)
    
    we get this. so google those capital keyword and see. so i got that BASE 65536 is binary encoding optimised for UTF-32 and BASE 64 is used for binary-to-text encoding.
Step 2:

    found this site that decode BASE 65536 and we get this 3 flag.
![welcome](/resource/zh3r0/mix3.png)
Source: https://www.better-converter.com/Encoders-Decoders/Base65536-Decode

Step 3:

    Again read main statement BASE 65536 is done then next capital keyword so this is a chain of encryption and solve the ctf.so user the cyberchef for that.
             
    Flag 1 is SHIFT KEYBOARD cipher but its is a first pard of flag.
            
**zh3r0{Y0u_sur3_**

![welcome](/resource/zh3r0/mix4.png)

Flag 2 is Hex -> Binary -> Normal keyword
            
**4r3_4w3s0m3_wi7h**    
      
![welcome](/resource/zh3r0/mix5.png)

![welcome](/resource/zh3r0/mix6.png)

Flag 3 is in BASE 64 -> SPOON Binary -> Normal keyword
      
**_411_7h3_ski115}**

![welcome](/resource/zh3r0/mix7.png)

![welcome](/resource/zh3r0/mix8.png)

Step 4:
    
    Combine all 3 Flag and submit

#### FLAG: zh3r0{Y0u_sur3_4r3_4w3s0m3_wi7h_411_7h3_ski115}

### 3.2 **RSA-Warmup**
![welcome](/resource/zh3r0/rsa1.png)

Step 1:
    
    Read statement carefully and find out given hints. so get remote server with it and connect and we get bellow output.
![welcome](/resource/zh3r0/rsa2.png)
```
 But there is catch when i try to connect that remote server it generate a diffrent values every time so use anyone output to crack. its a RSA Cryptography also mention in statement “RSA is one of the first public-key cryptosystems”. so there are tool to do that.
              
We have N, we have e, we have CT, No other information, This is most likely to be the generic RSA challenge where N is some special case factorizable. OKAY lets do this
 ```

 `p,q = 
(2942026403, 134575070417930364036003727741376685615812461954350484569708437014667994680713813781468183983386234011962070146684234011280627785955402931339880339689145836820522726630562036268896319664602063579145594582463191728917055827142635500611088623983035188866470062494891880603875253301899285045944864340088876075089)
`   

Since p was small   
Source :   http://factordb.com/

#### Flag : zh3r0{RSA_1s_Fun}

## 4. Web
### 4.1 **Web-Warmup**
![welcome](/resource/zh3r0/web1.png)

Step 1:
    
    We have a link go there see what can you find there.nothing on page .so got to inspact elements and see any odd things.
![welcome](/resource/zh3r0/web2.png)
 
 Step 2:
 
    In style editer section we got our flag.just check out all section of inspact elements.

![welcome](/resource/zh3r0/web3.png)

#### Flag: zh3r0{y3s_th1s_1s_w4rmup}


