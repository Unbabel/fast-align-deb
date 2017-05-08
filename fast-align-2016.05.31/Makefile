all: build

clean:
	rm -rf build

build: clean
	mkdir build
	cd build && cmake .. && make

install: build
	install -m 0755 build/fast_align $(DESTDIR)/usr/bin

.PHONY: install	
