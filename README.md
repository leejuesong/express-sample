# express-sample
POST로 json 데이터 보내면 에코치는 샘플

# 설치

## Node.js & npm 설치하기
Windows OS에서는 WSL을 사용하는 것을 권장. (Microsoft Store에서 Ubuntu 설치)

### Ubuntu에 Node.js v12.x 설치하기
```
# Using Ubuntu
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
sudo apt-get install -y nodejs
```

## 본 패키지 설치하기
npm 패키지만 설치하면 끝.
```
# 프로젝트 루트에서 아래 명령어 실행
npm i
```

# 실행
실행하면 로컬 3000번 포트에서 본 웹서버가 실행됨.
만약 3000번 포트가 다른곳에서 실행중이라면, `.env` 파일에서 PORT값을 다른 포트번호로 수정.
```
npm start
```

# 테스트
```
# request
curl --request POST \
  --url http://localhost:3000/ \
  --header 'Content-Type: application/json' \
  --data '{"foo":"bar"}'

# response
{"foo":"bar"}
```

# 참고사항
node.js & express는 가장 쉽고 빠르게 웹서버를 사용할 수 있다고 생각함.
물론, 프로덕트 환경에서 사용하려면 클러스터나 프로세스매니저 설정, 안전한 코드 작성 등
할일이 많겠지만, 러닝커브도 낮고 EZ하다 생각하니 토이프로젝트로 조금 갖고 놀아보고 선택해도 될거같음.

## 읽어볼만한 문서

- Node.js 설치 : https://github.com/nodesource/distributions/blob/master/README.md
- Express : https://expressjs.com/ko/