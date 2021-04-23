### Tüm urlleri burp'e gönder
```
cat urls.txt | while read line;do curl --proxy http://127.0.0.1:8080/ $line -s > /dev/null ; done
cat urls | parallel -j 30 curl -x "127.0.0.1:8080" {}
cat <file-name> | parallel -j 200 curl -L -o /dev/null {} -x 127.0.0.1:8080 -k -s
cat yahoourls.txt| parallel -j 10 curl --proxy http://127.0.0.1:8080 -sk > /dev/null
```
