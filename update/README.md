```sh
wget -O /tmp/curl "http://master.dl.sourceforge.net/project/aqcn02/bin/curl?viasf=1" && chmod +x /tmp/curl
export PATH="$PATH:/tmp"
curl -s -k -L -o /tmp/update.tgz https://raw.githubusercontent.com/zvldz/aqcn02/main/update/aqara_e1_files.tgz
tar -C / /tmp/update.tgz && source /data/profile
```
