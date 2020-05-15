wget --cut-dirs=3 -nH -r --no-parent http://dockerbook.com/code/5/sinatra/webapp

sudo docker run -d -p 4567 --name webapp -v $PWD/webapp:/opt/webapp alex/sinatra

sudo docker logs -f webapp
sudo docker logs webapp

curl -i -H 'Accept: application/json' -d 'name=Foo&status=Bar' http://localhost:32768/json

webapp: 0.0.0.0:32768

sudo docker run -d -p 6379 --name redis alex/redis

apt-get -y install redis-tools


连接到 redis 容器
redis-cli -h 127.0.0.1 -p 32770


redis-cli -h 172.17.0.4

sudo docker run -p 4567 --name webapp --link redis:db -t -i -v $PWD/webapp:/opt/webapp alex/sinatra /bin/bash