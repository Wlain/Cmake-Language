add_library(mylib STATIC 
  include/mylib/mylib.h
  src/mylib.cpp
  src/impl/mylib_impl.cpp
  src/impl/mylib_impl.h
)

target_include_directories(mylib
  PRIVATE src
  PUBLIC include
)

target_compile_definitions(mylib
  PRIVATE FASTPATH
)
