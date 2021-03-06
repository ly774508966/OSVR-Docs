# Installing OSVR for OS X

There are two wasys of installing OSVR-Core in OS X: using Homebrew or compiling it manually. Unless you're planning to contribute code to OSVR-Core itself, installing with Homebrew is the easier method.

## Installing using Homebrew

If you don't already have Homebrew installed, install it first following the instructions at http://brew.sh/.
You may install OSVR for OS X using our Homebrew repository:

```bash
$ brew tap OSVR/osvr
$ brew install osvr-core --HEAD
```

Once you've installed OSVR-Core using Homebrew, you don't need to build it from source.

## Building OSVR from source

1. *Prerequisites.* The prerequisites may be installed using Homebrew. If you prefer to install them manually, the list of prerequisites follows:
  * [CMake](https://cmake.org/)
  * [Boost](http://www.boost.org/)
  * [OpenCV](http://opencv.org/)
  * [Python 2](https://www.python.org/)
  * [libfunctionality](https://github.com/osvr/libfunctionality)
  * [libusb](http://libusb.info)

2. *Acquire the source code.* Check out the source code from the [OSVR-Core repository](<%=repo_url 'OSVR-Core' %>).

3. *Create a build directory.* To keep the source repository clean of temporary and generated build files, create a separate directory to contain the build. We usually create a directory named `build` inside the OSVR-Core directory.

    ```
    $ mkdir build
    $ cd build
    ```

4. *Generate a Makefile.* Run CMake to generate a Makefile. Set the `CMAKE_INSTALL_PREFIX` variable to the location where you would like the OSVR files to be installed:

    ```
    $ cmake .. -DCMAKE_INSTALL_PREFIX=~/osvr
    ```

5. *Compile OSVR.* Navigate to the build directory you created in step 3 and run `make` to build OSVR. Optionally run `make install` to install the OSVR programs, libraries, and sample configuration files.

    ```
    $ make
    $ make install
    ```

## Next steps

<ul class="arrows">
    <li><a href="http://resource.osvr.com/docs/OSVR-Core/">Peruse the OSVR reference documentation</a></li>
    <li><a href="/doc/unity">Integrate OSVR with Unity</a></li>
    <li><a href="/doc/unreal">Integrate OSVR with Unreal</a></li>
    <li><a href="/doc/client">Integrate OSVR with your own application</a></li>
    <li><a href="/doc/plugin">Write an OSVR plugin</a></li>
</ul>

## Support

If you need further assistance with installing OSVR, email us at [`support@osvr.org`](mailto:support@osvr.org).


