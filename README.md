LISTEN_ADDR=0.0.0.0:9094 NAME="Ratings Page" ./fake-service
# http://localhost:9094/ui # browser
# curl http://localhost:9094 #  new terminnal # after 4 terminal run 

LISTEN_ADDR=0.0.0.0:9093 NAME="Details Page" ./fake-service

LISTEN_ADDR=0.0.0.0:9092 NAME="Reviews Page" UPSTREAM_URIS="http://localhost:9094" ./fake-service

LISTEN_ADDR=0.0.0.0:9091 NAME="Product Page" UPSTREAM_URIS="http://localhost:9092,http://localhost:9093" ./fake-service
