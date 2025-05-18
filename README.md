lol# Fabrication-
# HYPERLEDGER FABRIC 

**Hyperledger Fabric is a modular, open-source blockchain framework, part of the Hyperledger project hosted by the Linux Foundation, designed for enterprise use cases, offering a permissioned network and focus on privacy and scalability.**
![image](https://github.com/user-attachments/assets/91fa2ff5-1ef8-4a16-b823-c5909fd48c88)

# 1. Install Go Programming Language

### sudo apt install golang-go ###

![fabrication 1](https://github.com/user-attachments/assets/082cc7fc-019f-4343-92b1-2dd52827d260)
![fb 3](https://github.com/user-attachments/assets/b42b5935-ab32-4b77-bb5f-9ecb1addbce7)



# Check Docker Version

### docker --version ###
![fb 2](https://github.com/user-attachments/assets/d06c3e18-ffa7-46f8-8cc9-91fb9073ff95)



# 


### fabric cloning ###
![fb4](https://github.com/user-attachments/assets/db7aaff8-979f-4aa2-8d72-e0df45b0a57e)



#  List Directory Contents

### change directory to test network


![fb5](https://github.com/user-attachments/assets/8e90b60b-10f1-4259-bff3-06a1b70be0bd)



### network.sh down

![fb6](https://github.com/user-attachments/assets/b5c0719e-664f-4c27-98b1-75337b4de156)




### cd fabric- ###

![fb7](https://github.com/user-attachments/assets/11fe426f-afbd-42e8-8edf-438310734e92)

## check network script help
![fb7 1](https://github.com/user-attachments/assets/086d1240-08b9-4f1b-92f8-630e6b66bd93)







# . Create a Channel in the Network

![fb 8 create channel](https://github.com/user-attachments/assets/0739a397-fe51-49b8-a2b1-5c11084579d1)



### ./network.sh createChannel ###
![fb9](https://github.com/user-attachments/assets/23d025ef-c094-4cf7-a211-a1ee345bd1c8)


# 12. Shut Down the Network

### ./network.sh down ###

![fb10](https://github.com/user-attachments/assets/8fe9620f-f1f7-4320-a771-d933193393fe)


# **IPFS 
# **What is IPFS?**

 ![image](https://github.com/user-attachments/assets/08e9d9cf-9f8a-49da-85d2-c3289ffb61eb)

**IPFS (InterPlanetary File System) is a peer-to-peer distributed file storage system. It allows users to store and share files in a decentralized way, using content-based addressing instead of location-based URLs.**

**Key Features:**

**->Files are identified by cryptographic hashes.**

**->Supports versioning and offline-first design.**

**->Efficient bandwidth usage via deduplication.**

**->Nodes store and cache files they access.**

# Step by Step implementation of Commands.....

1.	Install the IPFS through WSL:``` wget https://dist.ipfs.tech/kubo/v0.32.1/kubo_v0.32.1_linux- 
            amd64.tar.gz```

2.	```tar -xvzf kubo_v0.32.1_linux-amd64.tar.gz```
	
3.	Kubo is a reference implementation of IPFS in Go:``` cd kubo```
  
4.	```ls```
   
5.	```sudo bash install.sh```
	
6.	```ipfs –version```
	
7.	```ipfs init```


![ipfs 1](https://github.com/user-attachments/assets/4725c9fe-42ed-4374-b968-8fc535ea5d73)
![ipfs  11](https://github.com/user-attachments/assets/19bd07a1-4d96-4c26-9adc-14e51b5de4cf)
#
ipfs daemon
``
![ipfs2](https://github.com/user-attachments/assets/2e1fe74b-31a9-44a6-900d-91f860f1e5e0)
![IP2 1](https://github.com/user-attachments/assets/d98bab28-8e4a-4480-ad6a-2de540d6900d)


	


10.	```On Browser: http:![Uploading ipfs .11.PNG…]()
//127.0.0.1:5001/webui```

![IP3](https://github.com/user-attachments/assets/85ed6126-cb2f-4bf6-9b3f-c53480228112)



    


10.	```To run ipfs daemon in background: ipfs daemon > ipfs.log 2>&1 &```
	
11.	```This is daemon ID: [1] 772```
	
12.	```Add file: echo "Hello, IPFS!" > hello.txt```
	
13.	```ipfs add hello.txt```

![IP4](https://github.com/user-attachments/assets/e4544b10-a774-4a07-9500-28ce2d852d7b)


14.``` ipfs cat <CID>```

15.	Add a directory: ```mkdir myfolder```
    
```echo "File 1 content" > myfolder/file1.txt```

```echo "File 2 content" > myfolder/file2.txt```

16.	```ipfs add -r myfolder```
	
17.	```ps aux | grep ipfs```
	
18.	```kill <PID>```

![IP5](https://github.com/user-attachments/assets/f142d4af-a968-4db4-a66e-6dec0bdccd0d)


![IP5 1](https://github.com/user-attachments/assets/92b02112-3de2-43d7-a86e-b04d9cbba82c)
![ip6](https://github.com/user-attachments/assets/f6c70b6a-783e-4326-82a6-599526a18576)



19.	```In Browser you can directly run this to see the IPFS: https://ipfs.io/ipfs/QmWd9cavD8UGZQcqYBVhZqs2Jure5W9cgxR7S6TC4StfZe```

![image](https://github.com/user-attachments/assets/7e9f5d08-d9b5-4c77-bcfc-57cb16ddb372)

# Privacy and encryption on IPFS through command line..

1.	```echo "Hello, IPFS!" > myfile.txt```
	
2.	```ipfs add myfile.txt
	openssl enc -aes-256-cbc -pbkdf2 -iter 100000 -salt -in myfile.txt -out myfile_encrypted.txt -pass pass:yourpassword```
	
3.	```ipfs add myfile_encrypted.txt```
	
4.	```cat myfile_encrypted.txt```
	
5.	```openssl enc -d -aes-256-cbc -pbkdf2 -iter 100000 -in myfile_encrypted.txt -out decrypted_file.txt -pass pass:yourpassword```
	
6.	```cat decrypted_file.txt```
	
7.	```ipfs add decrypted_file.txt```

![ip7](https://github.com/user-attachments/assets/871e5b89-ad73-46d9-9fc4-13d95e4ef39f)
