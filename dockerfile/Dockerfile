FROM chbrandt/isis3

MAINTAINER "Carlos H Brandt <carloshenriquebrandt gmail>"

ARG ASP_VERSION='2.6.2'
ARG ASP_ROOT="/opt/asp/${ASP_VERSION}"

RUN mkdir -p $ASP_ROOT \
    && TARBALL="StereoPipeline-${ASP_VERSION}-2019-06-17-x86_64-Linux.tar.bz2" 				\
    && URL="https://github.com/NeoGeographyToolkit/StereoPipeline/releases/download/v${ASP_VERSION}"	\
    && cd $ASP_ROOT 								\
    && curl -L -O "${URL}/${TARBALL}" 						\
    && tar  --strip-components 1 -xjf $TARBALL					\
    && rm ${TARBALL}

RUN echo "export PATH=${ASP_ROOT}/bin:\$PATH" >> /etc/profile

