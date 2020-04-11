# Rust on GBA

Docker image for building Rust on GameboyAdvance

## Example

- makefile

```
build:
	mkdir -p target
	arm-none-eabi-as src/crt0.S -o target/crt0.o
	cargo xbuild --target arm-none-eabi.json --release
	arm-none-eabi-objcopy -O binary target/arm-none-eabi/release/gba-sandbox hello.gba
```


```
$ docker run -v `pwd`:/code bokuweb/rust-gba
```
