FROM ubuntu:22.04

WORKDIR /app

RUN apt-get update && apt-get install -y \
    curl \
    python3 && \
    rm -rf /var/lib/apt/lists/* 

RUN curl -sSL https://install.python-poetry.org | python3 -

ENV PATH="/root/.local/bin:${PATH}"

COPY pyproject.toml poetry.lock* ./

RUN poetry install

CMD ["/bin/bash"]