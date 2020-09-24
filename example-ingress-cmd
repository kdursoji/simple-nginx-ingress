krishna@evoke:~$ minikube start
😄  minikube v1.12.2 on Ubuntu 20.04
✨  Using the virtualbox driver based on existing profile
👍  Starting control plane node minikube in cluster minikube
🔄  Restarting existing virtualbox VM for "minikube" ...
🎉  minikube 1.13.1 is available! Download it: https://github.com/kubernetes/minikube/releases/tag/v1.13.1
💡  To disable this notice, run: 'minikube config set WantUpdateNotification false'

🐳  Preparing Kubernetes v1.18.3 on Docker 19.03.12 ...
🔎  Verifying Kubernetes components...
🌟  Enabled addons: default-storageclass, storage-provisioner
🏄  Done! kubectl is now configured to use "minikube"
krishna@evoke:~$ minikube addons enable ingress

🔎  Verifying ingress addon...
🌟  The 'ingress' addon is enabled
krishna@evoke:~$ 
krishna@evoke:~$ kubectl get pods -n kube-system
NAME                                        READY   STATUS      RESTARTS   AGE
coredns-66bff467f8-6pp7p                    1/1     Running     1          2d
etcd-minikube                               1/1     Running     1          2d
ingress-nginx-admission-create-qgmf9        0/1     Completed   0          2m5s
ingress-nginx-admission-patch-rbc5q         0/1     Completed   0          2m5s
ingress-nginx-controller-69ccf5d9d8-9jkq9   1/1     Running     0          2m5s
kube-apiserver-minikube                     1/1     Running     28         2d
kube-controller-manager-minikube            1/1     Running     2          2d
kube-proxy-pp295                            1/1     Running     1          2d
kube-scheduler-minikube                     1/1     Running     1          2d
storage-provisioner                         1/1     Running     25         2d
krishna@evoke:~$ kubectl create deployment web --image=gcr.io/google-samples/hello-app:1.0
deployment.apps/web created
krishna@evoke:~$ kubecl get pod
^Ckrishna@evoke:~$ kubectl get pod
NAME                  READY   STATUS    RESTARTS   AGE
web-6785d44d5-pmfqc   1/1     Running   0          28s
krishna@evoke:~$ kubectl expose deployment web --type=NodePort --port=8080
service/web exposed
krishna@evoke:~$ kubectl get service
NAME         TYPE        CLUSTER-IP   EXTERNAL-IP   PORT(S)          AGE
kubernetes   ClusterIP   10.96.0.1    <none>        443/TCP          22h
web          NodePort    10.105.4.8   <none>        8080:31784/TCP   6s
krishna@evoke:~$ minikube service web --url
http://192.168.99.112:31784
krishna@evoke:~$ vi example-ingress.yaml
krishna@evoke:~$ ls
 Containerization                         minikube-linux-amd64.1
 Desktop                                  Music
 docker                                   nodejs-docker-example
 Documents                                Pictures
 Downloads                                Public
 example-ingress.yaml                     pycharm-professional-2020.2.1
 google-chrome-stable_current_amd64.deb   pycharm-professional-2020.2.1.tar.gz
 Java                                     PycharmProjects
 JavaWorkSpace                            Python
 kube                                     pyweb
'kube cmds'                               snap
 kuberenetes-demo-manifests-master        Templates
 kubernetes-ingress                       Videos
 Learnings                                working
 minikube-linux-amd64
krishna@evoke:~$ kubectl apply -f example-ingress.yaml
ingress.networking.k8s.io/example-ingress created
krishna@evoke:~$ kubectl get ingress
NAME              CLASS    HOSTS              ADDRESS          PORTS     AGE
cafe-ingress      <none>   cafe.example.com   192.168.99.112   80, 443   23h
example-ingress   <none>   hello-world.info   192.168.99.112   80        10s
krishna@evoke:~$ vi /etc/host
krishna@evoke:~$ vi /etc/host
krishna@evoke:~$ vi /etc/hosts
krishna@evoke:~$ sudo gedit /etc/host
host.conf    hostid       hostname     hosts        hosts.allow  hosts.deny
krishna@evoke:~$ sudo gedit /etc/hosts
[sudo] password for krishna: 

(gedit:160179): Tepl-WARNING **: 18:05:33.097: GVfs metadata is not supported. Fallback to TeplMetadataManager. Either GVfs is not correctly installed or GVfs metadata are not supported on this platform. In the latter case, you should configure Tepl with --disable-gvfs-metadata.
^C
krishna@evoke:~$ kubectl create deployment web2 --image=gcr.io/google-samples/hello-app:2.0
deployment.apps/web2 created
krishna@evoke:~$ kubectl expose deployment web2 --port=8080 --type=NodePort
service/web2 exposed
krishna@evoke:~$ kubectl apply -f example-ingress.yaml
error: error parsing example-ingress.yaml: error converting YAML to JSON: yaml: line 15: did not find expected key
krishna@evoke:~$ kubectl apply -f example-ingress.yaml
ingress.networking.k8s.io/example-ingress configured
krishna@evoke:~$ kubectl apply -f example-ingress.yaml
ingress.networking.k8s.io/example-ingress configured
krishna@evoke:~$ curl hello-world.info/v2
Hello, world!
Version: 2.0.0
Hostname: web2-8474c56fd-5rtjz
krishna@evoke:~$ curl hello-world.info
Hello, world!
Version: 1.0.0
Hostname: web-6785d44d5-pmfqc
krishna@evoke:~$ 


