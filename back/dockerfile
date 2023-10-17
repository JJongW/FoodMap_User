FROM node:16 
# 노드 공식이미지의 v16 사용하겠다.

WORKDIR /app 
# 이미지 내에서 워킹디렉토리 설정. ( = 우분투 cd 명령어 )
 
# COPY package*.json .
# COPY [ SRC : 호스트 OS 경로] [DEST : 이미지 상에서 경로 ]
# package로 시작해서 .json으로 끝나는 모든 파일을 app 디렉터리에 모두 복사해라
# ./ = workdir 설정때문에 /app/ 경로임

COPY . . 
# 현재 디렉토리 상의 모든 파일과 디렉터리를 앱디렉터리에 모두 복사해라.

RUN npm install
# run : 도커 이미지 빌드 상에서 해당 명령어 실행

EXPOSE 80 
# 도커 이미지가 어느 포트를 사용할지 ( 해당 포드 퍼블리싱 x. 도커 이미지 사용자에게 알려줌 )

CMD ["node", "index.js"]  