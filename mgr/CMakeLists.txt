set(SOURCES
  ../win32/registry.cpp
  ../win32/thread.cpp
  ../win32/synch.cpp
  ../win32/msgwnd.cpp
  ../win32/uuid.cpp
  ../win32/error.cpp
  ../win32/library.cpp
  ../win32/shmem.cpp
  ../log/log.cpp
  ../common/version.cpp
  main.cpp
  mgr.def
)

file(GLOB_RECURSE HEADERS "${CMAKE_SOURCE_DIR}/*.h*")

add_library(xfsmgr SHARED ${SOURCES} ${HEADERS})

target_link_libraries(xfsmgr rpcrt4 shlwapi)
