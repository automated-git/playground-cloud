# playground-cloud

Based on following repositories for simple testing of Argo CD :
https://github.com/paulbouwer/hello-kubernetes

https://github.com/argoproj/argo-cd

## Argo CD setup (with Kubernetes on windows)
Source/Instructions:
https://argo-cd.readthedocs.io/en/stable/getting_started/

### Installation of Argo CD:
```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

### Access to argo CD via portforwarding: (Load Balancing is not available on local kubernetes)
```
kubectl port-forward svc/argocd-server -n argocd 8080:443
```




custom messages can be changed in the values.yaml file

```
# Provide a custom message
message: "automated.ch changed the message! Argo CD Rocks"
```

## Argo CD with the hello-kubernetes deplyments
![image](https://user-images.githubusercontent.com/48131740/198001105-10b78849-b353-48ac-820a-41f31ed130c0.png)

## hello-kubernetes with custom message

![image](https://user-images.githubusercontent.com/48131740/198001523-19d18226-57df-4890-9de7-23026291a158.png)

