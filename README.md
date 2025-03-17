# FRP Setup

## Here we will learn how to setup FRP using your pc as a client server(server A) and AWS EC2 instance as proxy server(server B).
---
## First we will setup proxy server
### Step 1.
- launch a EC2 instance in aws.
  - allow security port 7000, 8080, 22, 80.
  ![image](https://github.com/user-attachments/assets/fd02de38-c7ca-4a0f-951a-057c6dae5c15)

### Step 2.
- Open AWS web CLI of your EC2 instance.
- Download the latest program for your operating system and architecture from the [Release](https://github.com/fatedier/frp/releases) page using "wget" command.
  - For example :
  ```
  wget https://github.com/fatedier/frp/releases/download/v0.61.2/frp_0.61.2_linux_amd64.tar.gz
  ```
- Extract the file using 'tar'.
  - For example :
  ```
  tar -xvzf frp_0.61.2_linux_amd64.tar.gz
  ```
- get inside the directory using 'cd'.
  - For example :
  ```
  cd frp_0.61.2_linux_amd64
  ```
      
### Step 3 : start proxy server
- open your frps.toml
  ```
  nano frps.toml
  ```
- configure your frps.toml
  ```
  bindPort = 7000
  auth.token = "my-secret-key"
  ```
- Start your proxy server
  ```
  ./frps -c frps.toml
  ```
### After all this you will get this 
![Screenshot from 2025-03-15 18-01-30](https://github.com/user-attachments/assets/19b57fa0-7750-41ed-baa1-8c65934f8143)

---

## now we will setup client server 

### Step 1.
- Open CLI of your pc.
- Download the latest program for your operating system and architecture from the [Release](https://github.com/fatedier/frp/releases) page using "wget" command.
  - For example :
  ```
  wget https://github.com/fatedier/frp/releases/download/v0.61.2/frp_0.61.2_linux_amd64.tar.gz
  ```
- Extract the file using 'tar'.
  - For example :
  ```
  tar -xvzf frp_0.61.2_linux_amd64.tar.gz
  ```
- get inside the directory using 'cd'.
  - For example :
  ```
  cd frp_0.61.2_linux_amd64
  ```


      
    
