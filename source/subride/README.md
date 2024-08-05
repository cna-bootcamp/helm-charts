# Subride 

## 소개
구독관리 서비스 

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
  ```
  replicaCount: 1
  ingress:
    hosts:
      - host: gappa.config.43.200.12.214.nip.io
        paths:
          - path: /
            pathType: ImplementationSpecific
  ```
  
- 설치  
  ```
  helm install {release nmae} [-f {custom config file}] subride/subride
  helm install config -f config/deployment/value.yaml subride/subride
  ```  
  
## 애플리케이션 삭제  

```
helm delete {release name}
```

## Configuration
