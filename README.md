# CClutterGtk
A wrapper around clutter-gtk for Swift

## Troubleshooting
Here are some common errors you might encounter and how to fix them.

### Old Swift toolchain or Xcode
If you get an error such as

	$ ./build.sh 
	error: unable to invoke subcommand: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/swift-package (No such file or directory)
	
this probably means that your Swift toolchain is too old.  Make sure the latest toolchain (Swift 3.0 at the time of this writing) is the one that is found when you run the Swift compiler, e.g.:

	$ swiftc --version
	Apple Swift version 3.0 (swiftlang-800.0.49 clang-800.0.40)
	Target: x86_64-apple-macosx10.9

  If you get an older version, make sure that the right version of the swift compiler is found first in your `PATH`.  On macOS, use xcode-select to select and install the latest version, e.g.:

	sudo xcode-select -s /Applications/Xcode.app
	xcode-select --install
