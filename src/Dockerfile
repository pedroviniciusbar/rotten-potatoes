FROM python:3.8-slim-buster
WORKDIR /app
COPY requirements.txt /app
RUN python -m pip install -r requirements.txt
COPY . /app
EXPOSE 80
CMD ["gunicorn"], "--workers=3", "--bind", "0.0.0.0:80", "app:app"]