Creamos los objetos statefulset y service.

Ejecutamos los objetos con las siguientes instrucciones:

kubectl apply -f service.yaml

kubectl apply -f statefulset.yaml

![alt text](https://github.com/jordill14/kube-exercises2/blob/master/hw-03/exercise_2/images/state.PNG)

Ejecutamos el pod creado con la siguiente instrucción:

kubectl exec -it mongo-0 -c mongo bash
