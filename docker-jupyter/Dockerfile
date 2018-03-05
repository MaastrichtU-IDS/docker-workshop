FROM ubuntu:latest

LABEL maintainer "Pedro Hernandez <p.hernandezserrano@maastrichtuniversity.nl>"
LABEL maintainer "Alexander Malic <alexander.malic@maastrichtuniverstity.nl>"

COPY docker-jupyter /root/docker-jupyter

RUN apt-get update && \
    apt-get -y install wget python-pip python2.7 python-dev python-matplotlib libblas3 liblapack3 libstdc++6 python-setuptools && \
    apt-get clean && \
    pip install --upgrade pip && \
    pip install seaborn && \
    pip install turicreate ipython "ipython[notebook]" jupyter

WORKDIR /root/docker-jupyter

EXPOSE 8888

CMD ["jupyter", "notebook", "--port=8888", "--no-browser", "--allow-root", "--ip=0.0.0.0"]
