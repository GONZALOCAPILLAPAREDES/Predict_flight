FROM mongo

COPY . .
RUN apt-get update
RUN apt-get install -y git
RUN apt-get install -y curl
RUN git clone https://github.com/ging/practica_big_data_2019.git
RUN practica_big_data_2019/resources/download_data.sh
RUN mv origin_dest_distances.jsonl data/origin_dest_distances.jsonl
#RUN ./practica_big_data_2019/resources/import_distances.sh

EXPOSE 27017

CMD ["sh","setup.sh"]