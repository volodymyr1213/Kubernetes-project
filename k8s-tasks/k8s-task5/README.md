# Kubernetes-task5
Task 5

A) Create group of apps which serve WordPress:
   - StatefulSets:
	* Name: wordpress-sts
	* 5 replicas
	* Use wordpress:4 image
   - MySQL ReplicaSet:
	* Name: mysql-rs
	* 1 replica
	* Use mysql image
   - Expose Wordpress using LoadBalancer service

B) Rollout wordpress-sts to wordpress:latest image
