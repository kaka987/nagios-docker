# nagios-docker
nagios-docker

# cd /path-to-nagios

# git clone https://github.com/kaka987/nagios-docker.git

# cd nagios-docker

# start the nagios docker
docker run -d --name nagios4 -v /path-to-nagios/nagios-docker/etc:/usr/local/nagios/etc -p 0.0.0.0:25:25 -p 0.0.0.0:8080:80 quantumobject/docker-nagios

# edit the etc add some server to monitor
