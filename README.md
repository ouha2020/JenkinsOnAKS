
# Jenkins on AKS 

## 環境要求
- kubernetes  v1.23.0

- Helm 3.0+

  

## 本地Domain追加 

```
  IP地址加到HOST文件
  192.168.1.121  jenkins.cicd.com
```

 可以使用SwitchHosts更加方便

![](/doc/SwitchHosts.png)

![](/doc/domain.png)

### 安裝

```
helm upgrade --install --create-namespace devops-storage ./devops-storage/ -f values.yaml  -n devops-apps

helm upgrade --install --create-namespace devops-apps-roles ./devops-apps-roles/  -f values.yaml  -n devops-apps

helm upgrade --install --create-namespace devops-apps ./devops-apps/  -f values.yaml  -n devops-apps

helm upgrade --install --create-namespace devops-apps-route ./devops-apps-route/  -f values.yaml  -n devops-apps
```





