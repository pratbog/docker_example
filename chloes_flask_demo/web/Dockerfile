FROM ubuntu:latest
RUN apt-get update -y
RUN apt-get install -y software-properties-common
RUN apt-add-repository universe
RUN apt-get update -y
RUN apt-get install -y apt-transport-https 
RUN apt-get install -y python3-pip python-dev build-essential
COPY . /app
WORKDIR /app
RUN python3 -m pip install -r requirements.txt
ENTRYPOINT ["python3"]
CMD ["app.py"]
