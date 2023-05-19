FROM python:3.9
RUN pip3 install redis
WORKDIR /usr/src/app
ADD . .
EXPOSE 8081

CMD ["python3" , "/usr/src/app/main.py"]