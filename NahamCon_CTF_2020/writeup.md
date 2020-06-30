# CTF Writeup : NahamCon CTF 2020
Author: tg
## 1. Warmup
### 1.1 **Read The Rules**
![nahamcon](/resource/NahamCon/read1.png)
Step 1:
    
    Open given link see what you can find. open inspact and you will see a flag.
![nahamcon](/resource/NahamCon/read2.png)

#### Flag:  flag{we_hope_you_enjoy_the_game}     
### 1.2 **CLIsay**
![nahamcon](/resource/NahamCon/cli1.png)
 
 Step 1:
 
    Download given file see what we can find in it.push than file in cyberchef and we find out that file is a ELF (Executable and Linkable Format) so that will work on linux.

![nahamcon](/resource/NahamCon/cli2.png)
 
 Step 2:
 
    Using stiring command you will find our flag. strings command will print all hunam readble char format from file.
 ![nahamcon](/resource/NahamCon/cli3.png)
#### Flag: flag{Y0u_c4n_r3Ad_M1nd5} 
### 1.3 **Metameme**
![nahamcon](/resource/NahamCon/met1.png)

Step 1:
    
    First read statement provided in CTF “Hacker memes. So meta”. so may be flag is in the METADATA of file.

![nahamcon](/resource/NahamCon/met2.png)

 using exiftool you get your flag.
 #### Flag: flag{N0t_7h3_4cTuaL_Cr3At0r}

### 1.4 **Mr. Robot**
![nahamcon](/resource/NahamCon/mr1.png)

Step 1:
    
    Read the statement you will get hint from name of the CTF Mr.Robot. may be robot.txt file.simple go to given url and search robot.txt file.or you can use dirb,gobuster etc.

![nahamcon](/resource/NahamCon/mr2.png)
#### Flag: flag{welcome_to_robots.txt}
### 1.5 **UGGC**
![nahamcon](/resource/NahamCon/u1.png)

Step 1:
    
    CTF is to become a Admin and get the flag. so Question is how to become admin. tried SQL Injuction but no work.may be we have to do with a session management.so do inspact element goto Network section

![nahamcon](/resource/NahamCon/u2.png)

Step 2:
    
    we get that we have a GET request may be we can manipulate some value.in header response of GET request we get a Cookie=gt
![nahamcon](/resource/NahamCon/u3.png)

 `Edit the same request and replace Cookie=gt with admin`
 
Step 3:
    
    In response section we get a weird word  
![nahamcon](/resource/NahamCon/u4.png)

 Step 4:
    
    any random input as username is get converted into Caesar Cipher so admin is converted into nqzva again set cookie as admin in Caesar Cipher so may be we can access as a admin.
![nahamcon](/resource/NahamCon/u5.png)
and Yes we get our flag !!!
#### Flag: flag{H4cK_aLL_7H3_C0okI3s}     
### 1.6 **Pang**
![nahamcon](/resource/NahamCon/pan1.png)

Step 1:
    
    Read statement and download attachment.first we dont no file extension.so open CyberChef and find out.
![nahamcon](/resource/NahamCon/pan2.png)
`Its PNG file`

Step 2:
    
    Just add .png and file will get open 
![nahamcon](/resource/NahamCon/pan3.png)

#### Flag : flag{wham_bam_thank_you_for_the_flag_maam}
## 2. Miscellaneous
### 2.1 **Vortex**
![nahamcon](/resource/NahamCon/v1.png)

Step 1:
    
    Actully i got this flag accidently.i dont no what to do i simple open browser and open URL like this.always try to open given URL in browser may be you get your answer easily.
![nahamcon](/resource/NahamCon/v2.png)
just did Ctrl + F with flag keyword and we got flag
#### Flag: flag{more_text_in_the_vortex}
