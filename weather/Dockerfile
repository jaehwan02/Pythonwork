FROM python:3.10

# 2. 작업 디렉토리 설정
WORKDIR /app

# 3. 필요한 파일 복사
COPY main.py /app/main.py
COPY requirements.txt /app/requirements.txt

# 4. 필요한 라이브러리 설치
RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 8000

# 5. Uvicorn으로 FastAPI 실행
CMD ["fastapi", "dev", "main.py", "--host", "0.0.0.0", "--port", "8000"]