Creamos los objetos deploy, service, replicaset y ingress y los ejecutamos:

![alt text](https://github.com/jordill14/kube-exercises2/blob/master/hw-03/exercise_1/images/ex1.PNG)

Creamos un certificado mediante OpenSSL:

openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -days 365 
-nodes -subj "//CN=jordi.student.lasalle.com//O=jordi.student.lasalle.com"

![alt text](https://github.com/jordill14/kube-exercises2/blob/master/hw-03/exercise_1/images/openssl.PNG)

Creo el secret que tiene el certificado antes creado:

![alt text](https://github.com/jordill14/kube-exercises2/blob/master/hw-03/exercise_1/images/secret.PNG)




