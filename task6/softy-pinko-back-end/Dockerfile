FROM ubuntu:latest

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y python3 python3-pip python3-flask python3-flask-cors

WORKDIR /app
COPY ./api.py /app/api.py

EXPOSE 5252

CMD ["python3", "api.py"]
