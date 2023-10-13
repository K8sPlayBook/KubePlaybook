1 : 
List one or more pods
command : kubectl get pod

2 : 
Delete a pod
command : kubectl delete pod <pod_name>

3 : 
Display the detailed state of a pods
command : kubectl describe pod <pod_name>

4 : 
Create a pod
command : kubectl create pod <pod_name>

5 : 
Execute a command against a container in a pod
command : kubectl exec <pod_name> -c <container_name> <command>

6 : 
Get interactive shell on a a single-container pod
command : kubectl exec -it <pod_name> /bin/sh

7 : 
Display Resource usage (CPU/Memory/Storage) for pods
command : kubectl top pod

8 : 
Add or update the annotations of a pod
command : kubectl annotate pod <pod_name> <annotation>

9 : 
Add or update the label of a pod
command : kubectl label pod <pod_name>

10 : 
delete the label of a pod
command : kubectl label pod <pod_name>

