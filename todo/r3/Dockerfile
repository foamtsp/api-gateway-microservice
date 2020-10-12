FROM python:3.7-buster
WORKDIR /root
RUN git clone https://github.com/natawutn/todo.git
WORKDIR /root/todo
RUN git checkout tags/release-3
RUN pip install -r requirements.txt
EXPOSE 8000
ENV REDIS_HOST redis
ENV NOTIFICATION_HOST notification
CMD python -m uvicorn --host=0.0.0.0 --port=8000 --reload todo.main:app
