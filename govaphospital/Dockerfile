FROM hyperledger/fabric-ca:latest

LABEL  maintainer="Thach Canh Nhut"

RUN rm -r /etc/hyperledger/fabric-ca-server

RUN mkdir /etc/hyperledger/fabric-ca-server

COPY fabric-ca-server-config.yaml /etc/hyperledger/fabric-ca-server

RUN mkdir /etc/hyperledger/fabric-ca-client

ENV FABRIC_CA_CLIENT_HOME=/etc/hyperledger/fabric-ca-client

COPY fabric-ca-client-config.yaml /etc/hyperledger/fabric-ca-client

EXPOSE 7055

CMD ["/bin/sh" "-c" "fabric-ca-server start -b rca-govap-org-admin:rca-govap-org-adminpw"]

