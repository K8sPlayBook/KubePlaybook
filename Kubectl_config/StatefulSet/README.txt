1 : 
List StatefulSet
command : kubectl get statefulset

2 : 
Create StatefulSet only (not pods)
command : kubectl Create statefulset/[stateful_set_name] --cascade=false

3 : 
Delete StatefulSet only (not pods)
command : kubectl delete statefulset/[stateful_set_name] --cascade=false

