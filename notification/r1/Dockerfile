FROM python:3.7-buster
WORKDIR /root
RUN git clone https://github.com/natawutn/todo-notification.git
WORKDIR /root/todo-notification
RUN git checkout tags/release-1.1
RUN pip install -r requirements.txt
EXPOSE 9000
ENV REDIS_HOST redis
CMD  python -m uvicorn --host=0.0.0.0 --port=9000 notification.main:app