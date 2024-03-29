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


![Diagrama]()

Nota : Este despligue se puede realizar en cualquier cluster de kubernetes cabe destacar que , se tiene que modificar la ubicacion del pv segun, se preferencia .

## Helm

![Diagrama]()

Nota : Este despligue se puede realizar en cualquier cluster de kubernetes cabe destacar que , se tiene que modificar la ubicacion del pv segun, se preferencia .

