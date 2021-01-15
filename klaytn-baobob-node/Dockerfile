FROM klaytn/klaytn

RUN apk update && apk add curl
RUN curl -X GET https://packages.klaytn.net/baobab/genesis.json -o ~/genesis.json

RUN ken --datadir ~/data init ~/genesis.json
COPY kend.conf /klaytn-docker-pkg/conf/kend.conf

EXPOSE 8551
CMD kend start
