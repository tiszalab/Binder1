FROM rocker/binder:4.5.1
LABEL maintainer='Ashleigh_Crawford'
COPY --chown=${NB_USER} . ${HOME}
USER ${NB_USER}



RUN wget https://github.com/tiszalab/Binder1/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2025-06-30/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
