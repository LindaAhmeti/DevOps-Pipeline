DevOps CI/CD Pipeline – Node.js | Docker | Jenkins | Kubernetes (Minikube)

Përshkrimi i Projektit
Ky projekt demonstron krijimin e një DevOps pipeline-i të plotë duke përdorur Jenkins, Docker, dhe Kubernetes (Minikube) për automatizimin e gjithë ciklit të zhvillimit të aplikacionit — nga kodimi deri te deploy-i final.

🎯 Qëllimet Kryesore

✅ Automatizim i ndërtimit dhe publikimit të aplikacionit
✅ Integrim i vazhdueshëm me Jenkins CI/CD
✅ Deploy automatik në Kubernetes (Minikube)
✅ Siguri përmes Docker Hub credentials në Jenkins

⚙️ Teknologjitë e Përdorura
Teknologjia	Përdorimi
Node.js	Zhvillimi i aplikacionit web
Docker	Containerizim i aplikacionit
Jenkins	CI/CD pipeline automation
Kubernetes / Minikube	Deploy i aplikacionit në mjedis lokal
GitHub	Menaxhim i versioneve dhe bashkëpunim

🧱 Struktura e Projektit
.
├── app.js
├── package.json
├── Dockerfile
├── Jenkinsfile
├── deployment.yaml
├── service.yaml
└── README.md
Pipeline-i ndërton një aplikacion Node.js, e containerizon me Docker, e publikon në Docker Hub, dhe më pas e deploy-on në Minikube për testim lokal.

💻 Aplikacioni Node.js
Një aplikacion i thjeshtë që shfaq mesazhin:
Hello from Linda Ahmeti DevOps Pipeline!

🐳 DockerfileNdërtimi manual:
docker build -t lindaahmeti/nodedockerpipeline .
docker run -p 3000:3000 lindaahmeti/nodedockerpipeline

⚙️ Jenkins Pipeline (CI/CD)
Ky Jenkinsfile përmban fazat kryesore të automatizimit:
Clone Repository – Merr kodin nga GitHub
Build Docker Image – Ndërton imazhin Docker
Login to Docker Hub – Autentifikim me kredenciale të sigurta
Push Image – Publikon imazhin në Docker Hub

☸️ Deploy në Minikube
Deploy manual në Minikube:
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

Shiko shërbimin:
kubectl get all
minikube service node-service

🧠 Rezultati Final
Pas ekzekutimit të pipeline-it në Jenkins:
Krijohet një imazh Docker nga aplikacioni
Imazhi publikohet automatikisht në Docker Hub
Aplikacioni vendoset në Minikube

Aksesoni në shfletues në:
http://<Minikube-IP>:30080


🟢 Do të shfaqet:

Hello from Linda Ahmeti DevOps Pipeline!
