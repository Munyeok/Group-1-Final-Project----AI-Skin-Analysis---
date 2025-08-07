# 사용할 기본 운영체제를 지정합니다.
FROM ubuntu:22.04

# 컨테이너 안에서 실행할 명령어를 정의합니다.
# 패키지 목록을 업데이트하고 필요한 프로그램을 설치합니다.
RUN apt-get update && apt-get install -y python3 python3-pip

# 작업 디렉토리를 설정합니다.
WORKDIR /app

# 로컬 PC의 모든 파일을 컨테이너의 /app 디렉토리로 복사합니다.
COPY . .

# 필요한 파이썬 라이브러리를 설치합니다.
RUN pip3 install -r requirements.txt

# 컨테이너가 시작될 때 실행할 기본 명령어를 설정합니다.
CMD ["python3", "app.py"]