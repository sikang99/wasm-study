

PROG=hello_world
#PROG=example

usage:
	@echo "make [edit|build|run|buikd-run]"

clean c:
	rm -f $(PROG).wasm

edit e:
	vi $(PROG).c

build b:
	emcc $(PROG).c -s WASM=1 -o $(PROG).html
b2:
	emcc -std=c++11 -pthread -s PROXY_TO_PTHREAD $(PROG).cpp -o $(PROG).js
run r:
	emrun --no_browser --port 8080 $(PROG).html

build-run br:
	emcc --emrun $(PROG).c -s WASM=1 -o $(PROG).html


git-update gu:
	cd ..; make gu

