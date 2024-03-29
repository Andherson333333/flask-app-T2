## Uso de este repositorio

Este repositorio contiene una aplicacion Tter 2 , y se puede desplegar de varias mananeras :

- Dockerfile
- Manifiesto kubernetes
- Charts de helm

## Requerimientos

- Instalacion docker y docker-compose
- Instalacion cluster kubernetes
- Instalacion de Helm

## Arquitectura cluster

El cluster donde se desplego este aplicativo tiene el siguiente diseño :

- Bastion host
- cluster kubernetes con 2 nodos 1 master
- Servidor NFS

![Diagrama]()
  
## Aplicacion flask 

Esta es una aplicación Flask simple que interactúa con una base de datos MySQL. La aplicación permite a los usuarios enviar mensajes, que luego se almacenan en la base de datos y se muestran en la interfaz.

![Diagrama]()

## Docker

![Diagrama]()

## Kubernetes

Para desplegar con los manfiesto tiene que ir a la carpeta llamada k8s-manifiesto hay se encuentran 2 carpetas con el siguiente nombre :

- flask-app
- mysql

Luego podemos entrar en cada una de ellas y lanzar el siguiente comando :

```
kubectl apply -f .
```
### Verificacion despliegue





![Diagrama]()

Nota : Este despligue se puede realizar en cualquier cluster de kubernetes cabe destacar que , se tiene que modificar la ubicacion del pv segun, se preferencia .

## Helm

Como estan en 2 charts de helm  por separados para modificar values , dentro de la siguiente  ruta se encuentra la aplicacion de python `flask-app-T2/flask-app-T2/helm/values.yaml` y en la siguiente ubicacion se encuentra los values de mysql  `flask-app-T2/flask-app-T2/helm/mysql-statefulset/values.yaml` 

Para desplegarlo en la con los charts de helm , hay que ir a la carpeta llamada helm y utilizar los siguientes comandos:
```
helm install flask-app-mysql mysql-statefulset/ && helm install flask-app-two-tier two-tier-flask-app/
```

### Verificacion del despligue
```
helm list
```

![Diagrama]()

Nota : Este despligue se puede realizar en cualquier cluster de kubernetes cabe destacar que , se tiene que modificar la ubicacion del pv segun, su preferencia .

