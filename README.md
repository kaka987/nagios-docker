# nagios-docker
nagios-docker

cd /home/young/github

git clone https://github.com/kaka987/nagios-docker.git

cd nagios-docker

docker run -d --name nagios4 -v /home/young/github/nagios-docker/etc:/usr/local/nagios/etc -p 0.0.0.0:25:25 -p 0.0.0.0:8080:80 quantumobject/docker-nagios

http://localhost:8080/nagios  nagiosadmin/admin


OR

docker run --name nagios4  \
  -v /home/young/github/nagios-docker/etc/:/opt/nagios/etc/ \
  -v /home/young/github/nagios-docker/custom_plugins:/opt/Custom-Nagios-Plugins \
  -p 0.0.0.0:8080:80 jasonrivers/nagios:latest

http://localhost:8080/nagios  nagiosadmin/nagios

docker exec -it bc392aa69e1b /usr/local/nagios/bin/nagios -v /usr/local/nagios/etc/nagios.cfg

