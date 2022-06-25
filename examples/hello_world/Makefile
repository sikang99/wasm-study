

PROG=hello_world

usage:
	@echo "make [edit|build|run|buikd-run]"

edit e:
	vi $(PROG).c

build b:
	emcc $(PROG).c -s WASM=1 -o $(PROG).html
run r:
	emrun --no_browser --port 8080 $(PROG).html

build-run br:
	emcc --emrun $(PROG).c -s WASM=1 -o $(PROG).html
