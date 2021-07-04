apiVersion: apps/v1
kind: Deployment
metadata:
 name: mavenwebappdeployment
spec:
 replicas: 2
 selector:
  matchLabels:
   app: mavenwebapp
 template:
  metadata:
   name: mavenwebapppod
   labels:
    app: mavenwebapp
  spec:
   containers:
   - name: mavenwebappcontainer
     image: ymanitheja12460/maven-web-application:12
     ports:
     - containerPort: 8080
---
apiVersion: v1
kind: Service
metadata:
 name: mavenwebappsvc
spec:
 selector:
  app: mavenwebapp
 type: NodePort
 ports:
 - port: 80
   targetPort: 8080
