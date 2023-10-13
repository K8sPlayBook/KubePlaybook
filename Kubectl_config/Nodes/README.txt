1 : 
Update the taints on one or more nodes
command : kubectl taint node <node_name>

2 : 
List one or more nodes
command : kubectl get node

3 : 
Delete a node or multiple nodes
command : kubectl delete node <node_name>

4 : 
Display Resource usage (CPU/Memory/Storage) for nodes
command : kubectl top node

5 : 
Resource allocation per node
command : kubectl describe nodes | grep Allocated -A 5

6 : 
Pods running on a node
command : kubectl get pods -o wide | grep <node_name>

7 : 
Annotate a node
command : kubectl annotate node <node_name>

8 : 
Mark a node as unschedulable
command : kubectl cordon node <node_name>

9 : 
Mark node as schedulable
command : kubectl uncordon node <node_name>

10 : 
 
Drain a node in preparation for maintenance
command : kubectl drain node <node_name>

11 : 
Add or update the labels of one or more nodes
command : kubectl label node

