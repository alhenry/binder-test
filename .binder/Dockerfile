FROM rocker/binder:3.6.0
LABEL maintainer='Albert Henry'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}



RUN wget https://github.com/alhenry/binder-test/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2019-08-26/')); devtools::install_deps()"

RUN rm DESCRIPTION.1
