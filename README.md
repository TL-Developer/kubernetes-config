# kubernetes-config
Kubernetes config

kind get clusters

kind create cluster --name nginx

kubectl config get-contexts

kubectl config use-context nginx-02

kubectl cluster-info --context kind-nginx

kind create cluster --name nginx --config cluster.yml

kubectl port-forward pod/pod_name 8080:80

To run locally, use Metallb with type ConfigMap Yaml

kubectl wait --namespace metallb-system --for=condition=ready pod --selector=app=metallb --timeout=90s


kubectl apply -f https://kind.sigs.k8s.io/examples/loadbalancer/metallb-config.yaml