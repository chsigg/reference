FROM tensorflow/tensorflow:1.12.0-devel-gpu-py3

COPY requirements.txt .
RUN pip3 install -r requirements.txt

ENV BOARD_SIZE="19"

ENTRYPOINT ["/bin/bash", "-c", "bazel run --config=opt \
  //:reinforcement -- --base_dir=$(pwd)/results/$(date +%Y-%m-%d)"]
