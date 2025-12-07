FROM ubuntu:22.04

WORKDIR /app

# システム依存関係のインストール
RUN apt-get update && apt-get install -y \
    curl && \
    rm -rf /var/lib/apt/lists/*


RUN curl -LsSf https://astral.sh/uv/install.sh | sh

ENV PATH="/root/.local/bin:${PATH}"

RUN uv python install 3.14.1

COPY . .

RUN uv sync

CMD ["/bin/bash"]