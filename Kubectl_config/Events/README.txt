1 : 
List recent events for all resources in the system
command : kubectl get events

2 : 
List Warnings only
command : kubectl get events --field-selector type=Warning

3 : 
 List events but exclude Pod events
command : kubectl get events --field-selector involvedObject.kind!=Pod

4 : 
 Pull events for a single node with a specific name
command : kubectl get events --field-selector involvedObject.kind=Node, involvedObject.name=<node_name>

5 : 
Filter out normal events from a list of events
command : kubectl get events --field-selector type!=Normal

