FROM base
ARG ZEPPELIN_URL=https://archive.apache.org/dist/zeppelin/zeppelin-0.6.2/zeppelin-0.6.2-bin-all.tgz
ARG ZEPPELIN_VER=zeppelin-0.6.2-bin-all

ARG SPARK_URL=https://archive.apache.org/dist/spark/spark-1.6.2/spark-1.6.2-bin-hadoop2.6.tgz
ARG SPARK_VER=spark-1.6.2-bin-hadoop2.6

RUN wget ${SPARK_URL} -O /spark.tgz
RUN tar -xzvf spark.tgz
RUN mv ${SPARK_VER} /spark

RUN wget ${ZEPPELIN_URL} -O /zeppelin.tgz
RUN tar -xzvf zeppelin.tgz
RUN mv ${ZEPPELIN_VER} /zeppelin
RUN echo "export SPARK_HOME=/spark" >> /zeppelin/conf/zeppelin-env.sh

ADD assets /assets
ADD assets/start_zeppelin.sh /start_zeppelin.sh

#CMD source /root/.bashrc; cd /spark; /zeppelin/bin/zeppelin.sh run
