#VERSION=1.3_v1
FROM maven:3.3.3-jdk-7

ENV SELDON_TAG v1.3-alpha.1
ENV SELDON_HOME /home/seldon
RUN mkdir -p  "$SELDON_HOME"
WORKDIR $SELDON_HOME
RUN (git clone https://github.com/SeldonIO/seldon-server --branch ${SELDON_TAG} && \
    cd seldon-server/offline-jobs/spark && \
    mvn package)

# Define default command.
CMD ["bash"]



