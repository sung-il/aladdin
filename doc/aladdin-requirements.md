aladdin 실행에 필요한 모니터링 컴포넌트들을 helm을 통해서 설치합니다. (node-exporter, kube-state-metrics)

    git install https://github.com/soda-infra/aladdin-requirements
    helm install aladdin-requirements --name aladdin-requirements

