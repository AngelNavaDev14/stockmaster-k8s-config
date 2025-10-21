# Configuración de Kubernetes para la Aplicación StockMaster 🚀

Este repositorio contiene todos los manifiestos de Kubernetes (`.yaml`) necesarios para desplegar el ecosistema de la aplicación `StockMaster` como una arquitectura de microservicios.

Este es un proyecto de **Infraestructura como Código (IaC)** que demuestra la capacidad de gestionar y orquestar una aplicación multi-contenedor de forma declarativa y reproducible.

## 🏗️ Arquitectura Desplegada
La configuración define y despliega los siguientes componentes en un cluster de Kubernetes:
1.  **Deployment de Base de Datos:** `Pod` con **PostgreSQL 15** y `Service` de tipo `ClusterIP`.
2.  **Deployment de la API de Productos:** `Pod` con la [**stockmaster-api**](https://github.com/AngelNavaDev14/stockmaster-api) y `Service` de tipo `NodePort`.

## 🛠️ Habilidades y Tecnologías Demostradas
*   **Orquestación:** Kubernetes (K8s)
*   **Contenerización:** Docker
*   **Infraestructura como Código (IaC):** Manifiestos YAML.
*   **Conceptos de Kubernetes:** `Deployments`, `Services` (`ClusterIP`, `NodePort`), `Pods`, `Labels`, `Selectors`, `Variables de Entorno`.

## 🚀 Cómo Desplegar
1.  Tener un cluster de Kubernetes funcional (probado con **K3s** y Minikube).
2.  Clonar el repositorio y aplicar los manifiestos con `kubectl apply -f .`.
3.  Acceder a la API usando `kubectl port-forward service/stockmaster-api-service 8080:8000`.
```4.  **Guarda el archivo (`Ctrl + S`).**