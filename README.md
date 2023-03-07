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
