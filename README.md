ALVAR - A Library for Virtual and Augmented Reality
---------------------------------------------------
This is a GCC 5.0 Competible source of ALVAR. Built and Tested on Ubuntu 16.04 system.

Compiling on Linux
----
These instructions were tested on Ubuntu 16.04. You can find the original instructions on building ALVAR
on other platforms in `doc` directory.

1. Setup a build environment.
     `apt-get install build-essential cmake`

2. Download and install OpenCV 2.4.0.

3. Install GLUT using distribution package or compile it yourself.
     `sudo apt-get install freeglut3-dev`
     
4. Optionally install OpenSceneGraph using distribution package or compile it
   yourself.
     `apt-get install libopenscenegraph-dev`

4. Run ./build/generate_[target].sh, where target is one of the following
   supported platforms.
     `gcc43: GNU Compiler Collection 4.3
     `gcc44: GNU Compiler Collection 4.4`
     `gcc45: GNU Compiler Collection 4.5 (experimental)`
     `gcc5: GNU Compiler Collection 5.0 (experimental)`

   Example:
     `cd ./build`
     `chmod +x generate*.sh`
     `./generate_gcc5.sh`

5. If CMake cannot find the required libraries, the cmakegui is launched.
   Configure the following variables accroding to your development
   environment.
     `OpenCV_ROOT_DIR = /path/to/opencv`
     `GLUT_ROOT_PATH = /usr`
     `OSG_ROOT_DIR = /usr`

   Press 'Configure' and modify the paths until the 'Generate' button is
   enabled. Press 'Generate' and close the cmakegui window.

6. Build the project.
     `cd ./build/build_gcc5_release`
     `make`

7. Optionally build the 'install' project to copy the sample and demo
   applications to the ./bin directory.
     `make install`


How to compile the ALVAR library SRC package
--------------------------------------------

When building from the source package, you have the option of using the
precompiled version of OpenCV provided by the OpenCV development team. The
CMake build system should be able to correctly find the dependencies if you
specify the OpenCV_ROOT_DIR variable.
  http://sourceforge.net/projects/opencvlibrary/files/opencv-win/2.4.0

The build instruction are basically the same as when building from the SDK
package.

The source package also contains 'master', 'build' and 'package' scripts in
the build directory. These are used to generate the SDK and BIN packages.


----
Original ReadMe Note from VTT
--

ALVAR is a software library for creating virtual and augmented reality (AR)
applications. ALVAR has been developed by the VTT Technical Research Centre
of Finland. ALVAR is release under the terms of the GNU Lesser General Public
License, version 2.1, or (at your option) any later version.

For compiling instructions, please see doc/Compiling.txt.

For release notes, please see doc/ReleaseNotes.txt

For additional information, please visit the ALVAR website or contact us.

VTT Augmented Reality Team
<http://www.vtt.fi/multimedia/alvar.html>
<alvar.info@vtt.fi>
