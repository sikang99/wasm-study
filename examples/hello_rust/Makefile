#
# Makefile for wasm rs
#
PROG=hello
usage:
	@echo "usage: make [edit|build|run]"

edit e:
	vi $(PROG).rs

build b:
	cargo build --target wasm32-wasi

run r:
	wasmtime $(PROG).wasm


git-update gu:
	cd ..; make gu




