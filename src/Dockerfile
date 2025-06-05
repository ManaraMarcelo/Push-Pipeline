FROM ubuntu:latest
WORKDIR /app
RUN apt-get update && \
    apt-get install -y python3 python3-pip
COPY . /app
RUN pip3 install -r requirements.txt --break-system-packages
EXPOSE 8000
CMD ["gunicorn", "-w", "4", "-b", "0.0.0.0:8000", "app:app"] 