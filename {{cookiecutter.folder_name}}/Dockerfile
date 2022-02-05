FROM condaforge/miniforge3:4.11.0-0

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update -y \ 
  &&  apt-get install -y build-essential make pkg-config libicu-dev curl\
  && rm -rf /var/lib/apt/lists/*


COPY requirements.txt $HOME
RUN pip install -r requirements.txt

WORKDIR $HOME/src
