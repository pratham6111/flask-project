FROM docker.io/python:3
WORKDIR /app
MAINTAINER prathameshmisal
COPY . .
RUN pip install -r requirements.txt
EXPOSE 5000
CMD ["python","app.py"]
