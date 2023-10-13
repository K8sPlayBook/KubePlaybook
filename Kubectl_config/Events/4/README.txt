4 : 
 Pull events for a single node with a specific name
command : kubectl get events --field-selector involvedObject.kind=Node, involvedObject.name=<node_name>

