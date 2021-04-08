# hash:sha256:39f32af7e5af0b166d78742f89f6774dd027c8b3dfcb4f6d4c678ccafb0c3a6a
FROM registry.codeocean.com/codeocean/miniconda3:4.7.10-cuda10.1-cudnn7-ubuntu18.04

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        g++=4:7.4.0-1ubuntu2.3 \
        gcc=4:7.4.0-1ubuntu2.3 \
        gettext=0.19.8.1-6ubuntu0.3 \
        libgettextpo-dev=0.19.8.1-6ubuntu0.3 \
    && rm -rf /var/lib/apt/lists/*

RUN conda install -y \
        backcall==0.1.0 \
        chardet==3.0.4 \
        cycler==0.10.0 \
        decorator==4.4.0 \
        filelock==3.0.12 \
        idna==2.8 \
        ipython==7.8.0 \
        jedi==0.15.1 \
        kiwisolver==1.1.0 \
        matplotlib==3.1.1 \
        numpy==1.17.2 \
        pandas==0.25.1 \
        parso==0.5.1 \
        pexpect==4.7.0 \
        pickleshare==0.7.5 \
        ptyprocess==0.6.0 \
        pygments==2.4.2 \
        pyparsing==2.4.2 \
        pysocks==1.7.1 \
        python-dateutil==2.8.0 \
        pytz==2019.3 \
        requests==2.22.0 \
        scipy==1.3.1 \
        seaborn==0.10.0 \
        six==1.12.0 \
        tqdm==4.36.1 \
        traitlets==4.3.3 \
        urllib3==1.25.8 \
        wcwidth==0.1.7 \
    && conda clean -ya

COPY postInstall /
RUN /postInstall
