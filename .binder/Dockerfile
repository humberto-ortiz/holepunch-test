FROM rocker/binder:4.3.0
LABEL maintainer='Humberto Ortiz-Zuazaga'
COPY --chown=${NB_USER} . ${HOME}
USER ${NB_USER}



RUN wget https://github.com/humberto-ortiz/holepunch-test/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2023-05-04/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
