
Strangely, if I simply run './configure' with no options, the resulting
Makefile doesn't build, on my Ubuntu 20 machine.

Instead I had to add a '--disable-precomp-headers' flag, to get a working build.

./configure --disable-precomp-headers


- ginobean, 06-dec-2021.

----
Interestingly, the default configuration seems to use gtk-2.0, and I am
seeing slow startup times of about 26-27 seconds, for the 'minimal' sample
app to even come up.

Switching to gtk-3.0 or X11, seems to resolve the aforementioned slow startup
issue, for the 'minimal' sample app (and, presumably, every other wxWidgets app).

gtk-3.0:

./configure --disable-precomp-headers --with-gtk=3


x11:
./configure --disable-precomp-headers --with-x11 --with-universal
