 # **What is IPFS?**

# Step by Step implementation of Commands.....

1.	Install the IPFS through WSL:``` wget https://dist.ipfs.tech/kubo/v0.32.1/kubo_v0.32.1_linux- 
            amd64.tar.gz```

2.	```tar -xvzf kubo_v0.32.1_linux-amd64.tar.gz```
	
3.	Kubo is a reference implementation of IPFS in Go:``` cd kubo```
  
4.	```ls```
   
5.	```sudo bash install.sh```
	
6.	```ipfs –version```
	
7.	```ipfs init```

   ![image](https://github.com/user-attachments/assets/713f4800-a5aa-42db-bc85-0a0446cf68ee)







   ![image](https://github.com/user-attachments/assets/425df7dc-f962-4a23-8f09-45630dec51e9)







   ![image](https://github.com/user-attachments/assets/625684b4-78ba-4214-9efa-1e6b95431f97)




  8.	```ipfs daemon```



   ![image](https://github.com/user-attachments/assets/8ae3835d-978c-4d9d-bab3-bca2b9bb936b)




9.	```On Browser: http://127.0.0.1:5001/webui```


    ![image](https://github.com/user-attachments/assets/ede35978-2458-446c-88b6-e5e68788ea1a)




10.	```To run ipfs daemon in background: ipfs daemon > ipfs.log 2>&1 &```
	
11.	```This is daemon ID: [1] 772```
	
12.	```Add file: echo "Hello, IPFS!" > hello.txt```
	
13.	```ipfs add hello.txt```



![image](https://github.com/user-attachments/assets/368ed43a-d00b-4a68-bb92-3fb777f0cf05)




14.``` ipfs cat <CID>```

15.	Add a directory: ```mkdir myfolder```
    
```echo "File 1 content" > myfolder/file1.txt```

```echo "File 2 content" > myfolder/file2.txt```

16.	```ipfs add -r myfolder```
	
17.	```ps aux | grep ipfs```
	
18.	```kill <PID>```



![image](https://github.com/user-attachments/assets/580af8a0-98a7-49c6-8b3a-483cd1e23c51)





![image](https://github.com/user-attachments/assets/a9626245-dea1-4960-932f-e1e66d0cdcee)




![image](https://github.com/user-attachments/assets/735ce917-111e-4a7b-a05d-18dded587a83)


19.	```In Browser you can directly run this to see the IPFS: https://ipfs.io/ipfs/QmWd9cavD8UGZQcqYBVhZqs2Jure5W9cgxR7S6TC4StfZe```

![image](https://github.com/user-attachments/assets/b734ab9c-13d9-422f-8d35-d53a04bc4b32)





# Privacy and encryption on IPFS through command line..

1.	```echo "Hello, IPFS!" > myfile.txt```
	
2.	```ipfs add myfile.txt
	openssl enc -aes-256-cbc -pbkdf2 -iter 100000 -salt -in myfile.txt -out myfile_encrypted.txt -pass pass:yourpassword```
	
3.	```ipfs add myfile_encrypted.txt```
	
4.	```cat myfile_encrypted.txt```
	
5.	```openssl enc -d -aes-256-cbc -pbkdf2 -iter 100000 -in myfile_encrypted.txt -out decrypted_file.txt -pass pass:yourpassword```
	
6.	```cat decrypted_file.txt```
	
7.	```ipfs add decrypted_file.txt```

![image](https://github.com/user-attachments/assets/9f170609-6fe6-4324-ba37-8ab718f6b015)

