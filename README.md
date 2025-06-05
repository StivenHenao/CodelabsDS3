
# 📂 Codelabs - Desarrollo de Software 3

  

Este repositorio contiene ejercicios prácticos basados en las guías de la materia **Desarrollo de Software 3**.

  

## 📁 Aprovisionamiento de una infraestructura

Este codelab cubre el aprovisionamiento de una infraestructura utilizando diversas herramientas y servicios:

-  **AWS**: Configuración de recursos en la nube.

-  **Bitvise**: Gestión de conexiones SSH.

-  **PostgreSQL por consola**: Administración y consultas en PostgreSQL desde la terminal.

-  **NGINX**: Configuración como servidor web y proxy inverso.

-  **C2S**: Configuración y gestión de la infraestructura.

  

## 📁 Comunicación entre microservicios

Explora la comunicación y descubrimiento de servicios en una arquitectura de microservicios mediante:

-  **Eureka Server**: Registro y visibilidad de los microservicios.

-  **OpenFeign**: Cliente HTTP declarativo para facilitar la comunicación entre microservicios.

  

## 📁 Comunicación asíncrona con RabbitMQ

Implementación de mensajería asíncrona utilizando RabbitMQ para la comunicación entre microservicios.

-  **Publicación y consumo de mensajes**: Ejemplo de envío de mensajes desde producto-service y recepción en pedido-service.

-  **Configuración de RabbitMQ**: Creación de exchanges, colas y bindings para garantizar la entrega de mensajes.

 ## 📁Kubernetes Nivel Intermedio

### Prerrequisitos
- Minikube
- Kubectl

### Comandos clave

1. Despliegue básico:
```bash
   kubectl apply -f webapp.yaml
   kubectl apply -f configmap.yaml
   kubectl apply -f secret.yaml
   ```

2. Verificar:
```bash
   kubectl get pods
   minikube service webapp-service
   ```

3. Multi-servicios:
```bash
   kubectl apply -f namespace.yaml
   kubectl apply -f auth-service.yaml
   kubectl apply -f pais-service.yaml
   ```

4. Limpieza:
```bash
   kubectl delete -f ./
   kubectl delete namespace auth-demo
   ```

### Extras
- Escalar: kubectl scale deployment/webapp --replicas=3
- Port-forward: kubectl port-forward svc/auth-service 8081:8080
  

🚀 Cada carpeta contiene los archivos y configuraciones necesarias para completar los ejercicios.