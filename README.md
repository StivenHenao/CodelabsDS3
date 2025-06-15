# 👨‍💻 Codelabs - Desarrollo de Software 3

  

  

Este repositorio contiene ejercicios prácticos basados en las guías de la materia **Desarrollo de Software 3**.

  

  

## 📁 Aprovisionamiento de una infraestructura

  

Este codelab cubre el aprovisionamiento de una infraestructura utilizando diversas herramientas y servicios:

  

-  **AWS**: Configuración de recursos en la nube.

  

-  **Bitvise**: Gestión de conexiones SSH.

  

-  **PostgreSQL por consola**: Administración y consultas en PostgreSQL desde la terminal.

  

-  **NGINX**: Configuración como servidor web y proxy inverso.

  

-  **C2S**: Configuración y gestión de la infraestructura.

  

  

## 📁 Comunicación entre microservicios Sincrónica Spring Boot

  

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

kubectl  apply  -f  webapp.yaml

kubectl  apply  -f  configmap.yaml

kubectl  apply  -f  secret.yaml

```

  

2. Verificar:

```bash

kubectl  get  pods

minikube  service  webapp-service

```

  

3. Multi-servicios:

```bash

kubectl  apply  -f  namespace.yaml

kubectl  apply  -f  auth-service.yaml

kubectl  apply  -f  pais-service.yaml

```

  

4. Limpieza:

```bash

kubectl  delete  -f  ./

kubectl  delete  namespace  auth-demo

```

  

### Extras

- Escalar: kubectl scale deployment/webapp --replicas=3

- Port-forward: kubectl port-forward svc/auth-service 8081:8080

  

## 📁 Github Actions

  
  

Trabajo de Github Workflows para ejecución de github Actions por medio del repositorio del microservicio de cliente-service. Este falla ya que no tiene las variables definidas para la base de datos, pero la verificación del workflow sirve.

  

## 📁 Kubernetes GCP

  

Codelab introductorio al despliegue de aplicaciones en Google Cloud Platform utilizando Kubernetes Engine:

  

- Habilitación de APIs: Activación del servicio Kubernetes Engine en GCP.

- Infraestructura: Creación de red virtual y subred para el clúster.

- Creación y conexión al clúster: Uso de gcloud y kubectl para gestionar el clúster.

- Despliegue del backend: Subida de contenedores y verificación del estado de las imágenes.

  

## 📁 Pruebas de integración en Spring Boot

  

Este codelab muestra cómo implementar y ejecutar pruebas de integración en una aplicación Spring Boot utilizando:

  

- MockMvc: Para simular peticiones HTTP y verificar las respuestas del controlador sin levantar el servidor.

- Spring Boot Test: Carga el contexto de la aplicación para pruebas completas.

- JPA y H2 en memoria: Permite pruebas con persistencia sin depender de una base de datos externa.

- Tests integrados: Se valida el correcto funcionamiento de endpoints como /hola/{nombre} y la consulta de entidades Pais desde la base de datos.

  

🔍 Se aseguran escenarios reales de interacción entre capas (controlador, servicio y repositorio), validando respuestas HTTP y contenidos JSON.

  ### 📁 Proceso con enfoque ADD y Clean Architecture

Este codelab explora cómo diseñar e implementar una arquitectura basada en atributos de calidad mediante **Attribute-Driven Design (ADD)**, y cómo estructurarla con **Clean Architecture**.

Se identificaron atributos clave del sistema (rendimiento, seguridad, disponibilidad) y se aplicaron tácticas arquitectónicas específicas. Luego, se implementó una solución modular y desacoplada con capas bien definidas (Dominio, Aplicación, Infraestructura, Presentación).

🔍 El proceso incluyó análisis, diseño, codificación y validación, destacando la importancia de alinear la arquitectura con los objetivos del negocio, la escalabilidad y el mantenimiento del sistema.


## 📁 Clean Architecture en microservicios Spring Boot

Este codelab implementa Clean Architecture dentro de un microservicio Spring Boot. Las capas están bien definidas y desacopladas, lo que facilita la escalabilidad, mantenimiento y pruebas. Se utilizó un ejemplo completo basado en una entidad `Producto`, con estructura en capas:

-   `domain/`: contiene entidades y repositorios abstractos.
    
-   `application/usecase/`: contiene los casos de uso como `ListarProductosUseCase`.
    
-   `infrastructure/persistence/`: implementación de repositorios JPA.
    
-   `delivery/`: controladores REST.
    
    Se aplicaron principios SOLID y los beneficios clave incluyen independencia tecnológica, separación de responsabilidades y facilidad para añadir nuevas funcionalidades sin romper las existentes.
----

🚀 Cada carpeta contiene los archivos y configuraciones necesarias para completar los ejercicios.