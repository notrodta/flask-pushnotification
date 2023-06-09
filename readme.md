# Documentation

* Follow the article:
* https://raturi.in/blog/webpush-notification-using-python-and-flask/

virtualenv -p python3 venv  

source venv/bin/activate

pip install -r req.txt

openssl ecparam -name prime256v1 -genkey -noout -out vapid_private.pem

openssl ec -in ./vapid_private.pem -outform DER|tail -c +8|head -c 32|base64|tr -d '=' |tr '/+' '_-' >> private_key.txt

openssl ec -in ./vapid_private.pem -pubout -outform DER|tail -c 65|base64|tr -d '=' |tr '/+' '_-' >> public_key.txt


#   f l a s k - p u s h n o t i f i c a t i o n 
 
 
