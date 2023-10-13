3 : 
 List events but exclude Pod events
command : kubectl get events --field-selector involvedObject.kind!=Pod

