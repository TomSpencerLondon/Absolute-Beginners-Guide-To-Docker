The Absolute Beginner's Guide to Docker
 • jonathan.m.turner@gmail
www.linkedin.com/in/jonathan-m-turner
 • Docker in dev vs. Docker in prod
 • Microservices - dockerise application
 • One way get value of docker is in development environment
 • Can run production code in docker - not what in this presentation
 • Docker for Windows & Docker for Mac
 • docker run - image file on computer to run containers
sudo docker run --rm -it anapsix/nyancat

sudo docker run --rm -d -p 1234:80 nginx

sudo docker run --rm -d -p 15672:15672 rabitmq:3-management

sudo docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres

sudo docker exec 4e bash

psql -U postgres

\dt

create table my_table (id varchar primary_key, int_value int, string_value varchar);
insert into my_table (id, int_value, string_value) values ('abc', 42, 'as string');

sudo docker-compose up -d
sudo docker-compose stop

```bash
tom@tom-ubuntu:~/Desktop/absolute-guide-to-docker$ sudo docker run --rm -it node bash
Unable to find image 'node:latest' locally
latest: Pulling from library/node
32fb02163b6b: Pull complete 
167c7feebee8: Pull complete 
d6dfff1f6f3d: Pull complete 
e9cdcd4942eb: Pull complete 
ca3bce705f6c: Pull complete 
4f4cf292bc62: Pull complete 
8347f8b4b86b: Pull complete 
c5f20f1b0856: Pull complete 
d220dfa3e187: Pull complete 
Digest: sha256:83841d113e09345a28b146e431f15b062341c5449218e501ba45ef8f9cff6049
Status: Downloaded newer image for node:latest
root@06368b093d93:/# node --version
v19.7.0
root@06368b093d93:/# echo "console.log('Hello world');" > app.js
root@06368b093d93:/# cat app.js
console.log('Hello world');
root@06368b093d93:/# node app.js
Hello world
root@06368b093d93:/# ls
app.js	bin  boot  dev	etc  home  lib	lib64  media  mnt  opt	proc  root  run  sbin  srv  sys  tmp  usr  var
```

sudo docker run --rm -it -v ${PWD}:/code python bash

```

tom@tom-ubuntu:~/Desktop/absolute-guide-to-docker$ sudo docker run --rm -it -v ${PWD}:/code python bash
Unable to find image 'python:latest' locally
latest: Pulling from library/python
32fb02163b6b: Already exists 
167c7feebee8: Already exists 
d6dfff1f6f3d: Already exists 
e9cdcd4942eb: Already exists 
ca3bce705f6c: Already exists 
5e1c6c4f8bbf: Pull complete 
efba3dc31239: Pull complete 
b45fafb4411c: Pull complete 
70eb3e954fe5: Pull complete 
Digest: sha256:d3c16df33787f3d03b2e096037f6deb3c1c5fc92c57994a7d6f2de018de01a6b
Status: Downloaded newer image for python:latest
root@eea5ace34d31:/# ls
bin  boot  code  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
root@eea5ace34d31:/# cd /code
root@eea5ace34d31:/code# ls
README.md  docker-compose.yml
root@eea5ace34d31:/code# echo "print(\"Hello world\")" > app.py
root@eea5ace34d31:/code# ls
README.md  app.py  docker-compose.yml
root@eea5ace34d31:/code# cat app.py
print("Hello world")
root@eea5ace34d31:/code# python app.py
Hello world
root@eea5ace34d31:/code# ^C
root@eea5ace34d31:/code# 
exit

```



