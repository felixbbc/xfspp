set(SOURCES
  ../win32/thread.cpp
  ../win32/synch.cpp
  ../win32/thread.cpp
  ../win32/timer.cpp
  ../win32/error.cpp
  ../win32/registry.cpp
  ../log/log.cpp
  dispatcher.cpp
  task.cpp
  main.cpp
  sp.def
)

file(GLOB_RECURSE HEADERS "${CMAKE_SOURCE_DIR}/*.h*")

add_library(test_sp SHARED ${SOURCES} ${HEADERS})
