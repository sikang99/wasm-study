

PROG=hello_clang

usage:
	@echo "make [edit|build|run|buikd-run]"

install i:
	@echo "make (install) [sdk|zig]"
install-sdk is:
	curl -O -sSL https://github.com/WebAssembly/wasi-sdk/releases/download/wasi-sdk-14/wasi-sdk-14.0-macos.tar.gz
	tar xf wasi-sdk-14.0-macos.tar.gz
install-zig iz:
	brew install zig
install-wasmtime iw:
	brew install wasmtime
	brew install wasmer
install-wagi ig:
	wget https://github.com/deislabs/wagi/releases/download/v0.8.1/wagi-v0.8.1-macos-amd64.tar.gz
install-wasienv ie:
	curl https://raw.githubusercontent.com/wasienv/wasienv/master/install.sh | sh

clean c:
	rm -rf $(PROG).wasm

edit e:
	vi $(PROG).c

build b:
	@echo "make (build) [1|2|3]"
b1:
	./wasi-sdk-14.0/bin/clang --sysroot wasi-sdk-14.0/share/wasi-sysroot/ $(PROG).c -o $(PROG).wasm
b2:
	clang --target=wasm32-wasi --sysroot=wasi-sdk-14.0/share/wasi-sysroot/ $(PROG).c -o $(PROG).wasm
b3:
	zig build-exe -O ReleaseSmall -target wasm32-wasi $(PROG).c -lc

run r:
	@echo "make (run) [1|2]"
r1:
	wasmtime $(PROG).wasm
r2:
	wasmer $(PROG).wasm
r3:
	wagi -c modules.toml


git-update gu:
	cd ..; make gu

