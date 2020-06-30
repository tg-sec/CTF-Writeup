# CTF Writeup
 Author: tg
## 1. Welcome
### **Brute Force 1.0** 
![Welcome](/resource/welcome.png)

Step 1:   
        
    This is simple Challenge we have to join Slack channel but flag is we can see in image.
  
#### Flag : HE{Welcome_to_Brute_Force_1_0}

## 2. Warm Up
### 2.1 **General 1**
![General 1](/resource/General1.png)

 Step 1:
    
    In given statement we have to change Hex value to ASCII value is `0x48`. do manualy or online.

![General 1](/resource/General1_2.png)

#### Flag : HE{H}

### 2.2 **General 2**
![General 2](/resource/General2.png)

Step 1:
    
    In given statement we have to convert Base 10 (`Decimal`) to Base 2 (`Binary`) that value will be our flag.

![General 2](/resource/General2_1.png)

#### Flag : HE{1001001100101100000001011010010}

### 2.3 **General 3**
![General 3](/resource/General3.png)

 Step 1:

    In given statement given value is string in HASH form but statement said that just only reverse it not to convert in a actually string.in CTF play you have to read statement carefully because mostly main hints are give in statement just we have to look carefully.for this we will use `CyberChef`.
![General 3](/resource/General3_1.png)

####  Flag: HE{17202b671953ed3ec4be52fd23f74901}

### 2.4 **General 4**
![General 4](/resource/General4.png)

Step 1:
    
    Read statement that say rotate the string may be this a kind of shift cipher so try them.and find out that is a  Caesar Cipher so we have online tool.
![General 4](/resource/General4_1.png)

Source : https://www.dcode.fr/caesar-cipher
#### Flag : HE{Rotate_Me_TO_Get_Points}   

### **General 5**
![General 5](/resource/General5.png)

Step 1:

    Read statement that is a SQL Dump and we have to find Name of Algorithm 

 `$pbkdf2-sha256$29000$7R3jfi/Xcfhvbjkdfgh.Jsangfjhmkl`

 key = pbkdf2(password, salt, iterations-count, hash-function, derived-key-len)

![General 5](/resource/General5_1.png)

Source : https://cryptobook.nakov.com/mac-and-key-derivation/pbkdf2 
#### Flag : HE{pbkdf2}**

### **General 6**
![General 6](/resource/General6.png)

 Step 1:
 
    See the image given in the Challenge . Its a kali logo/Image.

Source : https://www.kali.org/               
#### Flag : HE{kali} 

## 3. UNIX
### 3.1 **Grep**
![Grep](/resource/grep1.png)

Step 1:
    
    Read statement flag is in given file and that file contain some random text and we have to use GREP to catch the flag 
![Grep](/resource/grep1_1.png)

#### Flag : HE{ecfc468968534a32fe335bba396fa519}

## 4. Forensics
### 4.1 **Calculate**
![Calculate](/resource/Calculate.png)

 Step 1:
 
    Read given statement we have to calculate HASH of file so file in not tempared.use kali for this.
![Calculate](/resource/Calculate1.png)

#### Flag : HE{72375b80505890609cec28873201c9fa} 

## 5. Stegnography
### 5.1 **Copy Right and Comment**
![Calculate](/resource/Copy1.png)
Step 1:

     So in Challenge we have a JPEG file and we have to find flag which embeded in image.so i try with Steghide and image is password protected so we have to bruteforce the thing .

![Calculate](/resource/Copy2.png)

Step 2:

    I used stegcracker for bruteforce and rockyou.txt as worldlist so no use so i just look at the source of file and Yes flag was there.so lession is always try basic thing first.

![Calculate](/resource/Copy3.png)
 Source : https://github.com/Paradoxis/StegCracker  
 #### Flag : HE{7e69c214546a931d52312bb92da9d87d}

### 5.2 **M\*\*\*\*\* _ Code**

![code](/resource/code1.png)
Steg 1:

    Read statement and find the clues M***** _ Code and we have attach Image so it means may be kind of Morse code is embedded in that Image. Again do basic forensic on image and find out that image is password protected. Bruteforce is method.
![code](/resource/code2.png)
Source : https://github.com/Paradoxis/StegCracker

Step 2:

    We get a extracted file name Man.jpg.out and contain out Morse Code. decoe the morse code .
![code](/resource/code3.png)

**Decoded msg :**
![code](/resource/code4.png)

#### Flag : HE{PLAYING_WITH_MORSE_CODE}

## 6. Cryptography
### 6.1 **Brain Decode**
![code](/resource/decode1.png)

Step 1:

    Read statement and name of CTF that will give you a hint and its a crypto section and its a esoteric programming language and its Brainfuck cipher.

![code](/resource/decode2.png)

 Source : https://www.splitbrain.org/_static/ook/   
 Extra Source : https://en.wikipedia.org/wiki/Esoteric_programming_language
#### Flag : HE{c32f720f1a5eeae40201faeadcc4d96a} 

### 6.2 **De ------>> Code**
![code](/resource/de1.png)
Step 1: 
    
    See the contain try CyberChef. so we find out that its Base 64 encode in 7 time using same method .you have decode cipher seven time.Suggestion is alway try any cipher in CyberChef first.
![code](/resource/de2.png)
#### Flag : HE{Base64_Issssss_all_Time_favorite}

### 6.3 **Seven**
![code](/resource/seven1.png)

Step 1:

    Download the file see what contain in it. this is random alphanumaric data and we have hint is SEVEN so size of passwords bit is 7. I try muliple method but no outcome.after sometime i find out that its a password and got thre result as Cisco type 7 password.

Random data:    

    022E21405E555A711F1D5D48034416535C007F73767D31632362323635653363383931617D

![code](/resource/seven2.png)

Source : https://www.m00nie.com/type-7-password-tool/       
#### Flag : HE{53503341f3d80d5825b6ab265e3c891a}

### 6.4 **Nine**
![code](/resource/nine1.png)
Step 1:
    
    This is a similar CTF to the SEVEN just diffrence is that password was Cisco type 7 and this is Juniper type $9$ Hashed password.
![code](/resource/nine2.png)
 
Source : https://www.m00nie.com/juniper-type-9-password-tool/
#### Flag : HE{c6f518702470}
## 7. Miscellaneous
### 7.1 **Number Game**
![code](/resource/nu1.png)
Step 1:
    
    In the attachment we have a image and contain some numbers but may be in flag form.
![code](/resource/nu2.png)
Step 2:

    May be its really numbers game so pull out English alpha with numbers and we have numbers in image.
![code](/resource/nu3.png)

85{20 8 5_2 1 19 9 3_14 21 13 2 5 18_7 1 13 5}
HE{the_basic_number_game}

Source : https://www.worldometers.info/languages/how-many-letters-alphabet/
#### Flag : HE{the_basic_number_game}
              
### 7.2 **Break My Lock**
![code](/resource/lock1.png)

Step 1:
    
    Challenge name suggest us that we have to crack lock means have to do bruteforce. and we have a file attach that contain crackme.zip
![code](/resource/lock2.png)

Step 2:

    We will use john for crack a zip.notes.txt not contain anything.
![code](/resource/lock3.png)
![code](/resource/lock4.png)
after we break lock we get flag.txt file.We got our flag.

![code](/resource/lock5.png)

#### Flag : HE{7his_Chall3nG3_!s_$0_Eassssy}