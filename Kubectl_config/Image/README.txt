1 : 
kubectl get pods --namespace default --output jsonpath='{range .items[*]}{.spec.containers[*].image}{"\n"}{end}' | tr -s '[:space:]' '\n' | sort | uniq
command : kubectl get pods --namespace default --output jsonpath='{range .items[*]}{.spec.containers[*].image}{"\n"}{end}' | tr -s '[:space:]' '\n' | sort | uniq

