kubectl create deployment nginx --image=nginx
kubectl expose deployment nginx --port=80 --target-port=80
kubectl port-forward service/nginx 8080:80
create file <with required name>
{
  "forwardPorts": [8080]
}

