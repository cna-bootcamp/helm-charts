# Subride Front

## 소개
구독관리 서비스의 프론트엔드 애플리케이션  

## 사전준비
- Kubernetes 1.23.3+
- helm repository 추가  
  ```
  helm repo add subride https://cna-bootcamp.github.io/helm-charts/stable
  ```

## 애플리케이션 설치  
- 설치할 namespace로 이동  
  ```
  kubens {namespace}
  ex) kubens ondal
  ```   
- Configuration 파일 작성   
  
  
- 설치  
  ```
  helm install {release nmae} [-f {custom config file}] subride/subride-front 
  helm install front -f front.yaml subride/subride-front
  ```  
  
## 애플리케이션 삭제  

```
helm delete {release name}
```

## Configuration

The following table lists the configurable parameters of the chart and their default values.

| Parameter                                     | Description                                                                                                                                         | Default                                                 |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| `image.registry`                              | Image registry                                                                                                                                | `docker.io`                                             |
| `image.repository`                            | Image name                                                                                                                                    | `ondalk8s/hello-helm`                                         |
| `image.tag`                                   | Image tag                                                                                                                                     | `{TAG_NAME}`                                            |
| `image.pullPolicy`                            | Image pull policy                                                                                                                                   | `Always`                                          |
| `image.pullSecrets`                           | Specify docker-registry secret names as an array                                                                                                    | `nil`                                                   |
| `nameOverride`                                | String to partially override hello-helm.fullname template with a string (will prepend the release name)                                                  | `nil`                                                   |
| `fullnameOverride`                            | String to fully override hello-helm.fullname template with a string                                                                                      | `nil`                                                   |


