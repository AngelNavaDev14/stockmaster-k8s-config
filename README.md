# Configuración de Kubernetes para StockMaster API

Este repositorio contiene los manifiestos de Kubernetes (`YAML`) para desplegar el ecosistema de la aplicación `StockMaster` como una arquitectura de microservicios.

## 🏗️ Arquitectura Desplegada

La configuración despliega los siguientes componentes en un cluster de Kubernetes:

1.  **Deployment de Base de Datos:**
    *   Un Pod corriendo una instancia de **PostgreSQL 15**.
    *   Un **Service** (`postgres-service`) de tipo `ClusterIP` para exponer la base de datos de forma segura dentro del cluster.

2.  **Deployment de la API de Productos:**
    *   Un Pod corriendo la [StockMaster API](https://github.com/AngelNavaDev14/stockmaster-api), servida desde una imagen de **Docker**.
    *   Configurado con una **variable de entorno (`DATABASE_URL`)** para conectarse al `postgres-service`.
    *   Un **Service** (`stockmaster-api-service`) de tipo `NodePort` para exponer la API al exterior.

## 🛠️ Tecnologías Demostradas

*   **Orquestación:** Kubernetes (K8s)
*   **Contenedores:** Docker
*   **Infraestructura como Código (IaC):** Manifiestos YAML declarativos.
*   **Conceptos de K8s:** `Deployments`, `Services`, `Pods`, `Configuración de Red Interna`, `Variables de Entorno`.

## 🚀 Cómo Desplegar

1.  Clonar el repositorio: `git clone ...`
2.  Asegurarse de tener `kubectl` configurado para apuntar a un cluster.
3.  Aplicar todos los manifiestos: `kubectl apply -f .`

*Nota: Los manifiestos fueron probados en un cluster `kubeadm` y `Minikube`.*
