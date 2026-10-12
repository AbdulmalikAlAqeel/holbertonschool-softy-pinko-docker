FROM ubuntu:latest

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y python3 python3-pip

# Fix externally managed environment error for pip packages on newer Ubuntu versions
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask
RUN pip3 install flask

# Install Flask-CORS to allow cross-origin requests
RUN pip3 install flask-cors

WORKDIR /app

COPY ./api.py /app/api.py

CMD ["python3", "api.py"]
