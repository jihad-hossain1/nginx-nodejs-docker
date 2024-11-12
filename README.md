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
event {

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

