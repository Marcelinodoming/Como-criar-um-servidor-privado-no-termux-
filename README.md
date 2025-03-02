apt update

apt upgrade 

termux-setup-storage

pkg install root-repo

pkg install nodejs

pkg install openssl

openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout server.key -out server.crt

