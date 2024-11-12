- open docker desktop app
- open terminal and this command

```bash
docker ps
```
- then run this command
```bash
docker run -it -p 8080:80 ubuntu
```

- which mechanism to use? run this command 
```bash
uname -a
```
or 

```bash
 uname
```
- run this command for install sudo package
```bash
 apt-get update
```

- install nginx
```bash
 apt-get install nginx
```
- run this command for start nginx
```bash
nginx
```

- open browser and go to http://localhost:8080

- if you are not able to see the output of nginx please check your firewall settings.

- if you are using windows please check the file path of nginx

```bash
cd /etc/nginx

ls

ls -lh
```
- Edit this file or line '-rw-r--r-- 1 root root 1.5K Nov 30  2023 nginx.conf'

- install vim
```bash
 apt-get install vim
```

- run this command to open this file
```bash
vim nginx.conf
```

- backup this file
```bash
mv nginx.conf nginx_backup.conf
```

- create new file
```bash
touch nginx.conf

ls
```
- reload nginx
```bash
nginx -s reload
```

- run this command to open this file
```bash
vim nginx.conf
```
- press from keyboard 'i' for insert mode or type in vim editor

- write this line of code in the file
```bash
events {

}

http {
        server {
                listen 80;
                server_name _;

                location / {
                        return 200 "hello from nginx conf file";
                }
        }
}
```
- save this file with this command and exit
- cntrl + c
```bash
:wq
```
- then press ctrl + enter

- create a folder in /etc/nginx and create a index.html

```bash
mkdir website

cd website

touch index.html
```
- write html syntax
```bash
vim index.html
```
- save this file with this command and exit
- cntrl + c

```bash
:wq
```
- then press ctrl + enter

- see content 

```bash
cat index.html
```

- open nginx.conf file and edit

```bash
vim nginx.conf
```
- press from keyboard 'i' for insert mode or type in vim editor

```bash
events {
}

http {
        server {
                listen 80;
                server_name _;

                root /etc/nginx/website;
        }
}
```

- test configuration file ok

```bash
nginx -t

```
- reload nginx
```bash
nginx -s reload
```
- open browser and go to http://localhost:8080

- go to website folder and create a new file name of style.css 

```bash
cd website

touch style.css

vim style.css

```

- write this line of code in the file 

```bash
body {
        background-color: blue;
}
```

- save this file with this command and exit
- cntrl + c

- write this line of code in nginx.conf file

```bash
vim nginx.conf
```

```bash
events {
}

http {
        include /etc/nginx/mime.types;
        server {
                listen 80;
                server_name _;

                root /etc/nginx/website;
        }
}
```
