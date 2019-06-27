FROM golang
MAINTAINER Sudarshan Prajapati (sudarshan.praj@gmail.com)

#Installing dep
RUN go get -u github.com/golang/dep/cmd/dep

#cloning cadence-samples from remote repo into go/src
RUN cd src && git clone https://github.com/TeslaC-137/cadence-samples.git

# Extracting binary using make command
RUN cd src/cadence-samples && make

CMD cd src/cadence-samples/ && ./bin/helloworld -m worker

