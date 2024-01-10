# 이미지의 기본이 되는 이미지 선택
FROM node:14-alpine AS build-stage

# 작업 디렉토리 설정
WORKDIR /app

# 소스 코드 복사
COPY . .

# 애플리케이션 의존성 설치
RUN npm install

# 애플리케이션 빌드
RUN npm run build

# 최종 이미지 생성
FROM nginx:alpine

# 커스텀 nginx 설정 파일 복사
COPY nginx.conf /etc/nginx/nginx.conf

# nginx 설정 복사
COPY --from=build-stage /app/dist /usr/share/nginx/html

# 포트 설정
EXPOSE 80

# 컨테이너 시작 시 실행할 명령
CMD ["nginx", "-g", "daemon off;"]