FROM python:3.12.9-slim-bookworm

RUN apt-get update && apt-get install -y ghostscript

WORKDIR /code

COPY /src .

RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 8080

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8080"]
