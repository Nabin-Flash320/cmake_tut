# 2. MULTIPLE EXECUTABLES

There might some instances that a project might require multiple ***cpp*** files in same projects. To execute every one of them, the simplest method is to use multiple filenames after the main file that starts the project. The files are included in the ***add_executable()*** only as shown in this example.
```cmake
add_executable(executable_name file_1.cpp file_2.cpp ...)
```