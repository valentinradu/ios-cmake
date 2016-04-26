# iOS [CMake](http://cmake.com) Basic Build Configuration

This is a blank single-view-controller iOS app which uses CMake to create an XCode-friendly out-of-source build system. Instead of maintaining a `.xcodeproj` file, you instead maintain the CMakeLists.txt at the room of this directory to configure the build system for your iOS app.

CMake can do everything XCode can, but it easier to read the XCode's XML format, and easier to track in source control.

# To Use:
- Open `CMakeLists.txt`
  - Replace `your_project` on line 3 with your project name
  - Replace`com.yourcompany.yourprovisioning` on lines 23, 24, 25 with your bundle identifier
  - NOTE: the build will fail if you don't have provisioning profiles for that bundle identifier. It uses the 'iPhone Developer' code signing identity to avoid specifying a Certificate
- Install CMake with `brew install cmake`
- Configure `plist.in` for desired architectures, capabilities, orientations, etc
- run `build.sh` and your app should build.
- open `_builds/your_project.xcodeproj` for a full integrated XCode environment. Build and run as you ever would.

Happy hacking
