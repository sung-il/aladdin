aladdin 실행에 필요한 모니터링 컴포넌트들을 helm을 통해서 설치합니다. (node-exporter, kube-state-metrics)


#### 방법 1 (recommend)

    git install https://github.com/soda-infra/aladdin-requirements
    helm install aladdin-requirements --name aladdin-requirements


#### 방법 2

    helm repo add chartmuseum http://203.253.21.146:8080 (error 발생 시, helm init --client-only)
    helm install chartmuseum/aladdin-requirements --name aladdin-requirements
