# How to port pkgconf

```bash

./autogen.sh # add the missing m4 if needed

CC=/mnt/astraeaos/usr/bin/clang \
    ./configure \
        --build=x86_64-astraeaos-elf \
        --host=x86_64-astraeaos-elf \
        --prefix=/mnt/astraeaos/usr \
        --with-system-libdir=/mnt/astraeaos/lib:/mnt/astraeaos/usr/lib \
        --with-system-includedir=/mnt/astraeaos/usr/include

make && make install
```