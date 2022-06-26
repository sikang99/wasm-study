#
# Makefile
#
PROG=hello

usage:
	@echo "make [edit|build|run|buikd-run]"

clean c:
	rm -f $(PROG).wasm

edit e:
	vi $(PROG).gr
et:
	vi *.toml

build b:
	grain compile $(PROG).gr
run r:
	wasmtime hello.gr.wasm --env USER=mbutcher hello

web-server ws:
	wagi -c ./modules.toml
web-client wc:
	curl localhost:3000/hello-grain?hello=world



git-update gu:
	cd ..; make gu

