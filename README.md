# nextcloud-with-https-proxy
Nextcloud Personal cloud with https proxy

This is my docker compose file for creating a nextcloud server running with mariadb and a https proxy in front of it that passes all traffic from port 443 to the nextcloud instance running on port 80.

All images used in this project were the work of others and thank them in advance for their work.

Local Volumes

Create your local directory for the nextcloud data, and mariadb files

eg /nextcloud-with-https-proxy/data:/var/www/html

In the example above I have created a local host folder called /nextcloud-with-https-proxy/data which is mounted to /var/www/html within the container.

This will allow your uploaded files and data to remain persistent across reboots.

Cloning this repo will automatically create this for you and the data/mariadb folders with be created when you run the compose up for the first time:

In the example above I have created a local host folder called /nextcloud-with-https-proxy/data which is mounted to /var/www/html

docker-compose up -d from within /nextcloud-with-https-proxy

docker-compose up ## runs in the foreground

docker-compose up -d ## runs it as a background daemonised service.
