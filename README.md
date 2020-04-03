# THE SOURCE CODE HAS MOVED!! 
For the latest source code, go here: https://dev.azure.com/gabrielmcmillan/_git/limelight_library
The instructions below will still work however.

# limelight_library
A simple library to help make cleaner calls to the Limelight.<br/>
![I know this is in robotcontainer and I am not supposed to do that, but I needed a quick place to put it anyways.](ex.gif)

# How to use:
1. In your build.gradle file paste the following:
This part goes before the deploy call.
<pre>
repositories {
   maven {
    url 'https://pkgs.dev.azure.com/gabrielmcmillan/limelight_library/_packaging/limelight_library_maven/maven/v1'
}
}
</pre>
This part goes under dependancies.
<pre>
compile(group: 'com.fearxzombie', name: 'limelight_library', version: 'unspecified')
</pre>
2. Build your robot code to pull the dependancies.
3. In robot code: make a reference to limelight(); 
4. Use limelight.get**(); or limelight.set**(); to get or set NT values.

By default, the name is "limelight", however it can be changed by appending a string to the contructor.

This is an example robot project that uses the LimelightLibrary: https://github.com/fearxzombie/limelight_library_Example
