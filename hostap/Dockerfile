FROM zmqbase
ADD app /app
# WORKDIR /app
# RUN git clone git://github.com/samrussell/hostap
WORKDIR /app/hostap/eap_example
EXPOSE 4567
RUN make
CMD ./gary_example
