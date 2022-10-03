FROM ubuntu:22.10

RUN apt update
RUN apt install -y \
    git \
    make \
    binutils \
    openocd \
    doxygen \
    wget \
    unzip \
    python3-serial \
    gdb-multiarch

ARG RIOT_VERSION=2022.07
ENV RIOTBASE=/riot
RUN git clone -c advice.detachedHead=false --branch ${RIOT_VERSION} --depth 1 https://github.com/RIOT-OS/RIOT.git ${RIOTBASE}

ENV CONTAINER_PATH="${PATH}"

COPY fixpath /bin/
RUN touch /bin/fixpath.inc

ENTRYPOINT [ "/bin/fixpath"]
CMD ["bash"]

LABEL RUN="podman run --rm -it --name riot --env-host -v /home:/home -v /dev:/dev --workdir=\$PWD IMAGE"
