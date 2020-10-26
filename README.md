apiVersion: apps/v1 # for versions before 1.9.0 use apps/v1beta2
kind: Deployment
metadata:
  name: debianbase
spec:
  selector:
    matchLabels:
      app: debianbase
  replicas: 3
  template:
    metadata:
      labels:
        app: debianbase
    spec:
      containers:
      - name: frontend-client
        image: dockerguy20/debianbase:1
        #ports:
        #- containerPort: 80
        imagePullPolicy: Always

