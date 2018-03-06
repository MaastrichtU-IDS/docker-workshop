FROM ubuntu:latest

LABEL maintainer "Pedro Hernandez <p.hernandezserrano@maastrichtuniversity.nl>"
LABEL maintainer "Alexander Malic <alexander.malic@maastrichtuniverstity.nl>"

RUN apt-get update && \
    apt-get -y install wget python-pip python2.7 python-dev python-matplotlib libblas3 liblapack3 libstdc++6 python-setuptools && \
    apt-get clean && \
    pip install --upgrade pip && \
    pip install -U seaborn scikit-learn psycopg2 && \
    pip install turicreate ipython "ipython[notebook]" jupyter

WORKDIR /root

EXPOSE 8888

CMD ["jupyter", "notebook", "--port=8888", "--no-browser", "--allow-root", "--ip=0.0.0.0"]
