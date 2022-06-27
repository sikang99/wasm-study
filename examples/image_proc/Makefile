#
# Makefile for emcc
#

usage:
	@echo "make [build|run]"

build b:
	emcc -O3 – no-entry -s EXPORTED_RUNTIME_METHODS='["cwrap"]' -s NO_EXIT_RUNTIME=1 -s ALLOW_MEMORY_GROWTH=1 -o "./image.js" "./image.c" "./wasm.c"



git-updtae gu:
	cd ..; make gu
