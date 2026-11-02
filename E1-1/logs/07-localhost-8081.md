# 07. localhost:8081 접속 증거

Docker 컨테이너 `web-8081`(이미지 `e1-1-web:1.0`)을 `-p 8081:80`으로 띄우고, 같은 PC에서 접속했다.

## 1. 컨테이너 실행 상태

```
$ docker run -d -p 8081:80 --name web-8081 e1-1-web:1.0
$ docker ps --format "{{.Names}} {{.Image}} {{.Status}} {{.Ports}}"
web-8081 e1-1-web:1.0 Up 23 seconds 0.0.0.0:8081->80/tcp, [::]:8081->80/tcp
```

## 2. 응답 내용 (curl)

```
$ curl -s http://localhost:8081
<!doctype html>
<html lang="ko"><head><meta charset="utf-8"><title>E1-1 작업실</title></head>
<body><h1>E1-1 컨테이너 웹 서버</h1><p>Dockerfile로 만든 커스텀 nginx 이미지입니다. v1</p></body></html>

```

## 3. 브라우저 화면

브라우저에서 `http://localhost:8081`을 열었을 때 페이지 제목은 "E1-1 작업실"이고, 본문은 "E1-1 컨테이너 웹 서버"다. 캡처: [localhost-8081-page.jpg](../screenshots/localhost-8081-page.jpg)

