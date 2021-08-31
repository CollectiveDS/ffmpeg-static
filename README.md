FFmpeg static build
===================

Scripts to make a static build of ffmpeg with all the codecs required for a prod-fetch server.

Forked from a community-supported project and adapted for Studio71.

Just follow the instructions below. Once you have the build dependencies,
run ./build.sh, wait and you should get the ffmpeg binary in target/bin

Build & "install"
-----------------

    $ ./build.sh [-j <jobs>] [-B] [-d]
    # ... wait ...
    # binaries can be found in ./target/bin/

If you have built ffmpeg before with `build.sh`, the default behaviour is to keep the previous configuration. If you would like to reconfigure and rebuild all packages, use the `-B` flag. `-d` flag will only download and unpack the dependencies but not build.

Debug
-----

On the top-level of the project, run:

    $ . env.source

You can then enter the source folders and make the compilation yourself

    $ cd build/ffmpeg-*
    $ ./configure --prefix=$TARGET_DIR #...
    # ...


Related projects
----------------

* FFmpeg Static Builds - http://johnvansickle.com/ffmpeg/

License
-------

This project is licensed under the ISC. See the [LICENSE](LICENSE) file for
the legalities.

