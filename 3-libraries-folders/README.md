# Library and sub-directories

## Description
This will walk you through the cmake where a project is divided into multiple subdirectories.

## Walk through
1. The directory where the library is contained also requires a ***CMakeLists.txt*** file. Since it is not the root level cmake file, it should only contain following line of code.
   ```cmake
   add_library(library_name file_name)
   ```
2. On the root cmake file, some minor lines of codes should be changed.
   1. ```cmake
        add_subdirectory(sub_directory_name)
      ```
        This adds the sub-directory to be build for the project. The sub-directory must contain its own ***CMakeLists.txt** file.
   2. ```cmake
        target_include_directories(target INTERFACE|PRIVATE|PUBLIC include_folder)
      ```
      This specifies the include directories to be used while compiling the target. The INTERFACE|PRIVATE|PUBLIC are used to determine the scope of the include directories. Also, the target must be created uing add_executable() or add_library().
   3. ```cmake
        target_link_libraries(target library_name)
      ```
      This specifies the target libraries or the target files that are used when linking the given target.
    
   