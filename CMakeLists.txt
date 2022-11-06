cmake_minimum_required(VERSION 3.5)

project(helloworld)

add_executable(helloworld main.c)

include_directories("/opt/homebrew/Caskroom/miniforge/base/include/python3.9")

add_library(libpython3 SHARED IMPORTED)
set_property(TARGET libpython3 PROPERTY IMPORTED_LOCATION /opt/homebrew/Caskroom/miniforge/base/lib/libpython3.9.dylib)

target_link_libraries(helloworld libpython3)

# link_libraries(libpython3.9)
# link_directories(/opt/homebrew/Caskroom/miniforge/base/lib)
