# Best Buy Microservices Store

This project is a cloud-native microservices Best Buy application. The application demonstrates a distributed system using Kubernetes, Docker, and a microservices pattern to handle e-commerce operations including product management, ordering, and order processing.

##  Architecture Diagram

![Architecture Diagram](/architecture.png)

### Application Overview
The application is composed of five distinct microservices:
1.  **Store Front:** A Vue.js web application for customers to browse products and place orders.
2.  **Store Admin:** A Vue.js web application for employees/admins to manage products and view orders.
3.  **Order Service:** A backend service that processes incoming customer orders.
4.  **Product Service:** A backend service that manages the inventory and product details.
5.  **Makeline Service:** A backend service simulating the processing/fulfillment of orders.

##  Project Demo / YouTube Walkthrough

[**Click here to watch the demo video**]
(https://youtu.be/OWZJNxz1RcE)

##  Service Links & Docker Images

| Service | Docker Hub Image | Source Code (GitHub) |
| :--- | :--- | :--- |
| **Store Front** | [`anil0015/store-front-bb:latest`](https://hub.docker.com/r/anil0015/store-front-bb) | [Repository Link](https://github.com/anil0015/store-front-bb) |
| **Store Admin** | [`anil0015/store-admin-bb:latest`](https://hub.docker.com/r/anil0015/store-admin-bb) | [Repository Link](https://github.com/anil0015/store-admin-bb) |
| **Order Service** | [`anil0015/order-service-bb:latest`](https://hub.docker.com/r/anil0015/order-service-bb) | [Repository Link](https://github.com/anil0015/order-service-bb) |
| **Product Service** | [`anil0015/product-service-bb:latest`](https://hub.docker.com/r/anil0015/product-service-bb) | [Repository Link](https://github.com/anil0015/product-service-bb) |
| **Makeline Service** | [`anil0015/makeline-service-bb:latest`](https://hub.docker.com/r/anil0015/makeline-service-bb) | [Repository Link](https://github.com/anil0015/makeline-service-bb) |

---

##  Deployment Instructions

All Kubernetes manifests are located in the `Deployment Files/` folder.

### 1. Prerequisites
* A running Kubernetes cluster (Minikube, Docker Desktop, or Cloud Provider).
* `kubectl` command-line tool installed and configured.

### 2. Deploy to Kubernetes
Deploy all services, deployments, and statefulsets using the all-in-one manifest found in the deployment folder:

```bash
kubectl apply -f Deployment\ Files/BestBuy-all-in-one.yaml

```
### 4. Access the Application
Once the pods are running, you can access the application via the following URLs:

* **Store Front (Customer View):** [http://localhost](http://localhost)
* **Store Admin (Employee View):** [http://localhost:8081](http://localhost:8081)

---

##  Repository Structure
* `Deployment Files/`: Contains the `aps-all-in-one.yaml` and other Kubernetes manifests.
* `README.md`: Project documentation.