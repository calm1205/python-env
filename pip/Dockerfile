FROM ubuntu:22.04

WORKDIR /app

RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip \
    python3-venv && \
    rm -rf /var/lib/apt/lists/* && \

COPY requirements.lock .

RUN pip install -r requirements.lock

CMD ["/bin/bash"]