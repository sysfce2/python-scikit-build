cmake_minimum_required(VERSION 3.5...3.22)

project(hello)

find_package(PythonExtensions REQUIRED)

add_library(_hello MODULE hello/_hello.cxx)
python_extension_module(_hello)
install(TARGETS _hello LIBRARY DESTINATION hello)
