
FROM python:3.9-alpine

WORKDIR /app

COPY requirements.txt /app
COPY . /app

RUN python3 -m venv /app/venv && \
    /app/venv/bin/pip install --upgrade pip && \
    /app/venv/bin/pip install -r /app/requirements.txt


ENV PATH="/app/venv/bin:$PATH"

EXPOSE 8000

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]