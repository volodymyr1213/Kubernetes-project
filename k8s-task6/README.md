# Kubernetes_task6
Task 6

A) Create a Kubernetes Secret as follows:
	* Name: secret-creds
	* credential=MySecureP@ss
   Create a Pod named redis-pod, using the redis image, which mounts a secret named
   secret-creds at /app-creds, which exports credentials as SENSITIVE

B) Create below resources:
   - Create a Secret:
	* Name: mysql-credentials
	* credential= MySecureP@ss
   - MySQL deployment, exports Secret as MySQL_ROOT_PASSWORD
   - Expose it using a ClusterIP service, name it "db-service"

C) Create below resources:
   - Build a Docker image using below Dockerfile:
	FROM ubuntu:latest
	LABEL maintainer="Fname Lname (you@email.com)"
	RUN apt-get update -y && apt-get upgrade -y && apt-get install apache2 -y
	EXPOSE 80
	CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
   - Push it to DockerHub as a private image
   - Create a docker-registry Secret with DockerHub credentials
   - Create a replicaset with 3 replicas, which uses the image you have create in DockerHub,
   use Secret to pull the image.
