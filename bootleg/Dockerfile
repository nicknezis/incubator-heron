FROM heron/heron:0.17.8

WORKDIR /heron

RUN rm -rf /heron/* \
    /usr/local/heron

ADD heron-install.sh /heron/heron-install.sh

# run heron installer
RUN /heron/heron-install.sh \
    && rm -f /heron/heron-install.sh

RUN ln -s /usr/local/heron/dist/heron-core /heron \
    && mkdir -p /heron/heron-tools \
    && ln -s /usr/local/heron/bin /heron/heron-tools \
    && ln -s /usr/local/heron/conf /heron/heron-tools \
    && ln -s /usr/local/heron/dist /heron/heron-tools \
    && ln -s /usr/local/heron/lib /heron/heron-tools \
    && ln -s /usr/local/heron/release.yaml /heron/heron-tools \
    && ln -s /usr/local/heron/examples /heron \
    && ln -s /usr/local/heron/release.yaml /heron