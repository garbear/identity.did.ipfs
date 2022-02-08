cmake_minimum_required(VERSION 3.5)
project(identity.did.ipfs)

#list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)

# --- Add-on Dependencies ------------------------------------------------------

find_package(Kodi REQUIRED)

include_directories(
  ${PROJECT_SOURCE_DIR}/src
  ${KODI_INCLUDE_DIR}
)

set(IPFS_SOURCES
  src/addon.cpp
)

set(IPFS_HEADERS
  src/addon.h
)

# ------------------------------------------------------------------------------

build_addon(identity.did.ipfs IPFS DEPLIBS)

include(CPack)
