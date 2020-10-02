For rounded corners and kawase blurring were going to use

Some Required Values in your Picom.conf:

<div class='block'>
  <span class='badge'>corner-radius = 25</span>
  <span class='badge'>experimental-backends = true;</span>
  <span class='badge'>rounded-corners-exclude</span>
</div>

Correct Fork of Picom :
https://github.com/sdhand/picom

To build

$ git submodule update --init --recursive
$ meson --buildtype=release . build
$ ninja -C build

You can do that by setting the CPPFLAGS and LDFLAGS environment variables when running meson. Like this:

$ LDFLAGS="-L/path/to/libraries" CPPFLAGS="-I/path/to/headers" meson --buildtype=release . build
