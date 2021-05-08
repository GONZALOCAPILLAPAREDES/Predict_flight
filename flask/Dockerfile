FROM ubuntu:18.04

RUN apt-get update -y && \
    apt-get install -y python3.6 python3-pip git

WORKDIR /app

COPY . .

RUN git clone https://github.com/ging/practica_big_data_2019

RUN pip3 install -r /app/practica_big_data_2019/requirements.txt

RUN rm /app/practica_big_data_2019/resources/web/predict_flask.py

RUN mv /app/predict_flask.py /app/practica_big_data_2019/resources/web

ENV PROJECT_HOME /app/practica_big_data_2019

EXPOSE 5000

CMD ["python3", "/app/practica_big_data_2019/resources/web/predict_flask.py"]