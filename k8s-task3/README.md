# Kubernetes-task3
Task 3

A) Save the commands for below task in pv-commands.txt
	* List all persistant volumes by the name
	* List all persistent volumes sorted by size
   https://kubernetes.io/docs/reference/kubectl/cheatsheet/

B) Create a pod as follows:
	- Name: nginx-pod
	- Container image: nginx:1.14.0
	- Volume with name: data
	- Mount path: /usr/share/nginx/html

C) Create a persistent volume with name app-data, of capacity 1Gi and access mode ReadWriteOnce. 
   The type of the volume is hostPath and it`s location is /data/app-data/ 
   [Create the /data/app-data/ if it doesn`t exist]. Create a file index.html on /data/app-data with the content "Custom-Index".

D) Create a PersistentVolumeClaim named app-data-claim off of app-data persistent volume.

E) Create a pod as follows:
	- Name: nginx-app
	- Container image: nginx
	- PersistentVolumeClaim: app-data-claim
	- Mount path:/usr/share/nginx/html
