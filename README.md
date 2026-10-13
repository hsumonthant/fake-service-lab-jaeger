# Fake Service Lab

This lab uses Fake Service to build a simple service dependency flow.

## 1. Ratings Page

Run in Terminal 1:

LISTEN_ADDR=0.0.0.0:9094 NAME="Ratings Page" ./fake-service

Open in browser:

http://localhost:9094/ui

Open a new terminal and test with:

curl http://localhost:9094

## 2. Details Page

Run in Terminal 2:

LISTEN_ADDR=0.0.0.0:9093 NAME="Details Page" ./fake-service

Open in browser:

http://localhost:9093/ui

Open a new terminal and test with:

curl http://localhost:9093

## 3. Reviews Page

Run in Terminal 3:

LISTEN_ADDR=0.0.0.0:9092 NAME="Reviews Page" UPSTREAM_URIS="http://localhost:9094" ./fake-service

Open in browser:

http://localhost:9092/ui

Open a new terminal and test with:

curl http://localhost:9092

## 4. Product Page

Run in Terminal 4:

LISTEN_ADDR=0.0.0.0:9091 NAME="Product Page" UPSTREAM_URIS="http://localhost:9092,http://localhost:9093" ./fake-service

Open in browser:

http://localhost:9091/ui

Open a new terminal and test with:

curl http://localhost:9091

