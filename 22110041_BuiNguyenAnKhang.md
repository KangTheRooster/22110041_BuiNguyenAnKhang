# LAB #1,22110041,Bui Nguyen An Khang,INSE330380E_03FIE
## Task 1
Create a vulnerbility code
![alt text](image5.png)
![alt text](image-4.png)
Create a shell code c
![alt text](image-3.png)
![alt text](image-2.png)
Must conform to below structure:

Description text (optional)

- Compile both C programs and shellcode to executable code. 

- We need to change `void main` to `int main` in `shellcode.c`.

![image](./img0.png)

- Use an older shell and turn off randomly given stack value. 

![img](./img1.png)

- Create environmet variable `preload` with `export`.

![](./img2.png)

- Stack frame of `vuln.c`.

![](./stackframe.png)

- Use `gdb` to find the address of `system`, `exit` and `preload` variable.
  - Address of `system`: 0xf7e50db0
  - Address of `exet`: 0xf7e449e0
  - Adderss of `preload`: 0xffffde2c

![](./img3.png)

- Run `vuln.out` with command:

``` 
  r $(python -c "print('a'*20 + '\xb0\x0d\xe5\xf7' + '\xe0\x49\xe4\xf7' +  '\x2d\xde\xff\xff')")
```

output screenshot (optional)

**Conclusion**: The final results indicate that the combination of techniques environment variable and manipulation of memory space can lead to the execution of unauthorized actions within the system. This lab not only reinforces knowledge about security and software vulnerabilities but also emphasizes the importance of writing secure code to prevent similar attacks in real-world scenarios.

## Task 2
## Install bWapp
Install and run the website
![alt text](image-5.png)
![alt text](image-6.png)
Use http://localhost:8025/install.php?install=yes to open website
![alt text](image-7.png)
### Install SQL map

Use git clone https://github.com/sqlmapproject/sqlmap.git to clone sqlmap to your computer

![alt text](image-8.png)
![alt text](image-9.png)
### Question 1:
We must need a place where we can get the database by inject our code and login seems like a great choice
![alt text](image-10.png)
Now use F12 to inspect and get cookies
![alt text](image-12.png)
Use this comment to get database
![alt text](image.png)
We will get the results
![alt text](image-1.png)
### Question 2
To get tables we use 
![alt text](image-11.png)
![alt text](image-13.png)
![alt text](image-14.png)
![alt text](image-15.png)
And now to get user's accounts we use
![alt text](image-16.png)
We will get these results
![alt text](image-17.png)