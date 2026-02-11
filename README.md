# Quiz App 🧠

An interactive quiz application built using **HTML, CSS, and JavaScript**.  
This app allows users to answer multiple-choice questions with a **timer**, tracks their score, and displays a **result screen with a progress bar**.

---

## Features

- Multiple-choice questions with correct/wrong feedback  
- Timer for each question  
- Score tracking across all questions  
- Sound effects for correct and incorrect answers  
- Result screen with a green/red progress bar  
- Retry button to restart the quiz  

---

## Technologies Used

- HTML5  
- CSS3  
- JavaScript (ES6+)  
- Docker
- Kubernetes(KIND)


---


## Screenshots

### First Page
![First Page](images/first-page.png)

### Result Page
![Result Page](images/result-page.png)


---

🖥️ Run Project Locally (Without Docker)
✅ Step 1: Clone the Repository
git clone https://github.com/Lalit-Tiwa/Quiz-App.git
cd Quiz-App

✅ Step 2: Open in Browser

Simply open:

index.html


OR use Live Server in VS Code.

🐳 Run Using Docker
✅ Step 1: Build Docker Image
docker build -t quiz-app .

✅ Step 2: Run Container
docker run -d -p 8080:80 quiz-app

✅ Step 3: Access in Browser
http://localhost:8080

☸️ Deploy Using Kubernetes (KIND)
✅ Step 1: Install KIND and kubectl

Use the provided installation script
:

chmod +x kind.install.sh
./kind.install.sh

✅ Step 2: Create KIND Cluster

Use the configuration file:
./k8s/kind-config.yml

kind create cluster --config kind-config.yaml --name kind-cluster

✅ Step 3: Verify Cluster
kubectl get nodes
kubectl cluster-info

✅ Step 4: Apply Kubernetes Manifests

Go inside the k8s folder:

cd k8s
kubectl apply -f .


Verify resources:

kubectl get pods
kubectl get svc

✅ Step 5: Test From EC2 Itself
curl http://localhost:30080

✅ Step 6: Access From Browser
http://<EC2-PUBLIC-IP>:30080


Make sure:

Security Group allows port 30080

NodePort is correctly configured

📦 Kubernetes Architecture

Deployment → 2 replicas

Service → NodePort

Port Mapping → 30080

KIND cluster with custom configuration

🎯 What You Achieved

✅ Created KIND cluster with port mapping
✅ Deployed application with 2 replicas
✅ Exposed app using NodePort
✅ Opened Security Group
✅ Accessed app from browser

👨‍💻 Author

Lalit Tiwari
DevOps & Cloud Enthusiast 🚀
