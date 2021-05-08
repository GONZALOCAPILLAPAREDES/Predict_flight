FROM gettyimages/spark

EXPOSE 8080

COPY . . 

RUN ./sbin/start-all.sh

RUN apt-get update
RUN apt-get install git -y
RUN apt-get install python3-pip -y
RUN apt-get install zip -y
RUN curl -s "https://get.sdkman.io" | bash
RUN chmod a+x "/root/.sdkman/bin/sdkman-init.sh"
RUN /bin/bash -c "source /root/.sdkman/bin/sdkman-init.sh; sdk install java; sdk install sbt"


RUN git clone https://github.com/ging/practica_big_data_2019.git

RUN pip3 install -r practica_big_data_2019/requirements.txt

CMD ["sh", "comands.sh"]
