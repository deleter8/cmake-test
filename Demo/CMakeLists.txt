find_package(SFML COMPONENTS graphics window system REQUIRED)

# Make sure the compiler can find include files from our Hello library. 
include_directories (${HELLO_SOURCE_DIR}/Hello ${SFML_INCLUDE_DIRS} ) 

# Make sure the linker can find the Hello library once it is built. 
link_directories (${HELLO_BINARY_DIR}/Hello) 

# Add executable called "helloDemo" that is built from the source files 
# "demo.cxx" and "demo_b.cxx". The extensions are automatically found. 
add_executable (helloDemo demo.cpp) 

# Link the executable to the Hello library. 
target_link_libraries (helloDemo Hello ${SFML_LIBRARIES}) 
