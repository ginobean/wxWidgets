
Strangely, if I simply run './configure' with no options, the resulting
Makefile doesn't build, on my Ubuntu 20 machine.

Instead I had to add a '--disable-precomp-headers' flag, to get a working build.

./configure --disable-precomp-headers


- ginobean, 06-dec-2021.
