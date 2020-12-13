# Jenkins
1. docker pull jenkins/jenkins
2. docker run -d -p 8181:8080 -v /jenkins:/var/jenkins_home --name jenkins_container -u root jenkins/jenkins
3. browser 접속 (localhost:8181)
4. docker logs jenkins_container admin password 가져오기
5. 플러그인 설치
6. 로그인

- github 연동을 위한 rsa key pair 생성
1. docker exec -it jenkins_container /bin/bash
2. ssh-keygen
3. cd ~/.ssh
4. ls -al
5. .id_rsa.pub (공개키) github에 등록
6. github > settings > SSH and GPG keys > New SSH key
