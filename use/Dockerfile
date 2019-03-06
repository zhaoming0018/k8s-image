FROM ubuntu
RUN apt update && apt install -y bzip2 git wget && cd ~ && git clone https://github.com/csong27/ml-model-remember.git
RUN cd ~ && wget https://repo.anaconda.com/miniconda/Miniconda2-latest-Linux-x86_64.sh && sh Miniconda2-latest-Linux-x86_64.sh -b
RUN echo "export PATH=\$PATH:/root/miniconda2/bin" >> /root/.bashrc \
    && /miniconda2/bin/pip install theano==0.9.0 -i https://pypi.tuna.tsinghua.edu.cn/simple/ \ 
    && /miniconda2/bin/pip install cython -i https://pypi.tuna.tsinghua.edu.cn/simple/ && \ 
    /miniconda2/bin/pip uninstall lasagna && git clone https://github.com/Lasagne/Lasagne.git \
    && cd /root/Lasagne && /miniconda2/bin/python setup.py install
