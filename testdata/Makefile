## Makefile for Go example for Tarmac WASM functions

build:
	## Run TinyGo build via Docker because waPC requires a <0.18.0 version of TinyGo to work right
	docker run -v `pwd`/:/build -w /build tinygo/tinygo:0.17.0 tinygo build -o /build/tarmac.wasm -target wasi /build/main.go

docker-compose:
	docker compose up

run: build docker-compose
