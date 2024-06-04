# hash:sha256:459ba65b578c7109ef3a70eb3db5f10c77e1c7479e80c03ba5bce3ba55f1092a
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/py-r:python3.10.12-R4.2.3-IRkernel-ubuntu22.04

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN conda install -y --channel=conda-forge --channel=bioconda \
        anndata==0.9.2 \
        leidenalg==0.10.1 \
        matplotlib==3.7.2 \
        pandas==2.0.3 \
        scanpy==1.9.5 \
    && conda clean -ya
