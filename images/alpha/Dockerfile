FROM 0x0l/base:latest

ENV PYTHONIOENCODING UTF-8

RUN apt-get update \
 && apt-get install -y \
      curl \
      ffmpeg \
      g++ \
      gcc \
      gfortran \
      git \
      less \
      libblosc-dev \
      libedit-dev \
      libfreetype6-dev \
      libgmp-dev \
      libhdf5-dev \
      libjpeg-dev \
      libnetcdf-dev \
      libopenblas-dev \
      libpng3-dev \
      libssl-dev \
      libxml2-dev \
      libxslt-dev \
      libzmq3-dev \
      llvm-3.7-dev \
      pkg-config \
      python3 \
      python3-dev 

RUN curl https://bootstrap.pypa.io/get-pip.py > get-pip.py \
 && python3 get-pip.py \
 && rm get-pip.py

RUN pip install \
      Cython \
      numpy \
      numba

RUN LLVM_CONFIG=llvm-config-3.7 pip install \
      beautifulsoup4 \
      blosc \
      boto \
      bottleneck \
      cppimport \
      cufflinks \
      cvxpy \
      html5lib \
      ipyparallel \
      jupyter \
      keras \
      llvmlite \
      lxml \
      matplotlib \
      netCDF4 \
      networkx \
      nose \
      numba \
      numexpr \
      nltk \
      pandas \
      pandas-datareader \
      Pillow \
      https://github.com/quantopian/pyfolio/archive/master.zip \
      pykalman \
      https://github.com/pymc-devs/pymc3/archive/master.zip \
      qgrid \
      quandl \
      requests[security] \
      scipy \
      scoop \
      scrapy \
      sympy \
      tables \
      Theano \
      xarray \
      xlrd \
      xlwt \
      https://github.com/quantopian/zipline/archive/master.zip

ENV THEANORC /etc/theanorc:~/.theanorc
COPY theanorc /etc/theanorc

RUN jupyter nbextension enable --py widgetsnbextension
