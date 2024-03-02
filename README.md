# Kubernetes Exploration





# Commands

``` shell
# Choose project
cd ./clusters/<name cluster> #Ex: cd ./clusters/project01

# Choose name of cluster and export KUBECONFIG
export CLUSTER_NAME=dev-danilo1337 && export KUBECONFIG="/home/$USER/.kube/$CLUSTER_NAME"

# Create cluster
kind create cluster --name $CLUSTER_NAME --kubeconfig /home/$USER/.kube/$CLUSTER_NAME --config=config.yml

# Create namespaces 
kubectl create namespace development
kubectl create namespace shared
kubectl create namespace ingress-nginx

# Add the helm Chart for ingress-nginx
helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx && helm repo update

# Install nginx
helm install ingress-nginx -f ingress-values.yaml ingress-nginx/ingress-nginx -n ingress-nginx

# Run

kubectl apply -f deployment.yaml


# teste application http://localhost:30220/

```




``` text
         ,;;;,
       ;;;;;;;;
     ;;;;;;;;;;;;
    ;;;/\;;;;;;;;;
   ;;;     `,\;;;;;
  ;;;(        `,\;;
 ;;;(           `,\       # Danilo Ribeiro
 ;;;(           ,;'\      # Software Developer
 `;;(        ,;'';;;\     # Linkedin: danilo1337
  `;;;\    ,;;' ;;;;\     
    `;;;,;;'    \;;;;
      `;;'       \;;;
                  \;
```