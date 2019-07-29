## 알라딘 디버깅 

우선 수정한 소스를 빌드한다.

    make docker-build
    
생성된 이미지를 soda2019/aladdin로 푸쉬한다. 현재 이미지 태그는 dev로 통일, 태그(버전) 관리는 논의 후 최종 공지

    # docker login # docker hub에 로그인
    docker image tag kiali/kiali:dev soda2019/aladdin:dev
    docker push soda2019/aladdin:dev
   
푸쉬한 이미지를 기반으로 kiali deploy

    kubectl apply -n kiali-operator -f deploy/kiali/aladdin_cr.yaml
    
