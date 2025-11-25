FROM python:3.11-slim
WORKDIR /app

COPY inference.py main.py schemas.py utils.py requirements.txt .

RUN pip install -r requirements.txt

COPY models/trained/ models/trained/

EXPOSE 8000

CMD ["uvicorn", "app:main", "--host", "0.0.0.0", "--port", "8000"]