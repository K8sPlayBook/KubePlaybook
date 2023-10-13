1 : 
Print the logs for a pod
command : kubectl logs <pod_name>

2 : 
Print the logs for the last hour for a pod
command : kubectl logs --since=1h <pod_name>

3 : 
Get the most recent 20 lines of logs
command : kubectl logs --tail=20 <pod_name>

4 : 
Get logs from a service and optionally select which container
command : kubectl logs -f <service_name> [-c <$container>]

5 : 
Print the logs for a pod and follow new logs
command : kubectl logs -f <pod_name>

6 : 
Print the logs for a container in a pod
command : kubectl logs -c <container_name> <pod_name>

7 : 
Output the logs for a pod into a file named ‘pod.log’
command : kubectl logs <pod_name> pod.log

8 : 
View the logs for a previously failed pod
command : kubectl logs --previous <pod_name>

