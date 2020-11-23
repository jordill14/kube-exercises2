Creamos los objetos deploy, service y hpa.

Con la siguiente instrucción instalamos el addon metrics-server, para ver las métricas de la cpu:

minikube addons enable metrics-server

![alt text](https://github.com/jordill14/kube-exercises2/blob/master/hw-03/exercise_3/images/metrics.PNG)

Ejecutamos nuestros objetos con las siguientes instrucciones:

kubectl apply -f deploy.yaml

kubectl apply -f service.yaml

kubectl apply -f hpa.yaml

![alt text](https://github.com/jordill14/kube-exercises2/blob/master/hw-03/exercise_3/images/hpa.PNG)

Realizamos una prueba de estrés con la siguiente indtrucción:

kubectl run -i --tty load-generator --rm --image=busybox --restart=Never -- /bin/sh -c "while sleep 0.0000000001; do wget -q -O- http://IPSERVICE; done"

Para visualizar la carga utilizamos la siguiente instrucción:

kubectl get hpa nginx-hpa

![alt text](https://github.com/jordill14/kube-exercises2/blob/master/hw-03/exercise_3/images/gethpa2.PNG)



