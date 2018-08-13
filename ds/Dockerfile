FROM rajasoun/base:1.0
LABEL Vendor="DataScience"
MAINTAINER Raja. S <rajasoun@icloud.com>

ENV PACKAGES curl wget python3 octave gnuplot ttf-opensans ghostscript freetype-dev libpng-dev openblas-dev
ENV BUILD_ESSENTIAL make gcc g++ gfortran python3-dev 
ENV PIP_PACKAGE jupyter octave_kernel ipywidgets numpy scipy pandas matplotlib

COPY jupyter_notebook_config.py /root/.jupyter/jupyter_notebook_config.py

RUN echo "http://dl-cdn.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories \
    && apk add --no-cache --update ${PACKAGES} ${BUILD_ESSENTIAL} \
    && python3 -m venv /env/ \
    && /env/bin/pip install --upgrade pip \
    && /env/bin/pip install --no-cache-dir ${PIP_PACKAGE} \
    && /env/bin/jupyter nbextension enable --py --sys-prefix widgetsnbextension \
    && ln -s /usr/include/locale.h /usr/include/xlocale.h \
    && apk del ${BUILD_ESSENTIAL} \
    && rm -rf /var/cache/apk/* \
    && rm -rf /root/.cache/pip/*

VOLUME /opt/
EXPOSE 8888

# Init
ENTRYPOINT ["/init"]
CMD ["/env/bin/jupyter", "notebook", "--allow-root"]
