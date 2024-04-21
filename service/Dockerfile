FROM nvidia/cuda:12.1.0-base-ubuntu22.04

ENV PYTHONUNBUFFERED=1 

# system
# python3
RUN apt update -y -q && DEBIAN_FRONTEND=noninteractive apt install -y -q --no-install-recommends \
    software-properties-common apt-utils \
    curl git git-lfs vim \
    python3.10 pip libgl1-mesa-dev ffmpeg python3-pip python3-tk freeglut3-dev \
    && rm -rf /var/lib/apt/lists/*

# git
RUN git clone https://github.com/Anjok07/ultimatevocalremovergui.git /uvr5
#RUN git clone https://github.com/litagin02/laughter-collector.git /laughter-collector
WORKDIR /uvr5
RUN sed -i '/^Dora/d' requirements.txt

# requirements pytorch
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

# shell
COPY ./service/entrypoint.sh /tmp/entrypoint.sh
RUN chmod +x /tmp/entrypoint.sh
ENTRYPOINT ["/tmp/entrypoint.sh"]
