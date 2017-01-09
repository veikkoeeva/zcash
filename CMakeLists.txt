# Hints taken from http://www.slideshare.net/DanielPfeifer1/cmake-48475415.
cmake_minimum_required(VERSION 3.6 FATAL_ERROR)
set(CMAKE_VERBOSE_MAKEFILE ON)

# Sets the path to extra modules.
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_CURRENT_SOURCE_DIR}/cmake)


set(ZCASH_MAJOR_VERSION 1)
set(ZCASH_MINOR_VERSION 0)
set(ZCASH_PATCH_VERSION 4)
set(ZCASH_VERSION ${ZCASH_MAJOR_VERSION}.${ZCASH_MINOR_VERSION}.${ZCASH_PATCH_VERSION})

project(ZCash VERSION ${ZCASH_VERSION} LANGUAGES CXX C)

# Set Max OSX RPath explictitly. See more at https://blog.kitware.com/upcoming-in-cmake-2-8-12-osx-rpath-support/.
if(POLICY CMP0042)
  cmake_policy(SET CMP0042 NEW)
endif()

# https://cmake.org/cmake/help/v3.7/command/enable_testing.html
# enable_testing()


set(CPACK_PACKAGE_NAME ZCash)
set(CPACK_PACKAGE_DESCRIPTION_SUMMARY "ZCash description summary not yet written.")
set(CPACK_PACKAGE_VERSION_MAJOR ${ZCASH_MAJOR_VERSION})
set(CPACK_PACKAGE_VERSION_MINOR ${ZCASH_MINOR_VERSION})
set(CPACK_PACKAGE_VERSION_PATCH ${ZCASH_PATCH_VERSION})
set(CPACK_PACKAGE_VERSION ${ZCASH_VERSION})

include(FindGit)
if(GIT_FOUND AND EXISTS "${CMAKE_CURRENT_SOURCE_DIR}/.git")
  execute_process(COMMAND ${GIT_EXECUTABLE} rev-parse --short HEAD
    WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}
    OUTPUT_VARIABLE ZCASH_GIT_VERSION
    OUTPUT_STRIP_TRAILING_WHITESPACE)
else()
  message(STATUS "Warning: Git version info not found!")
endif()
add_definitions(-DZCASH_GIT_VERSION="${ZCASH_GIT_VERSION}")

# See rationale at https://crascit.com/2015/03/28/enabling-cxx11-in-cmake/.
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_SOURCE_DIR}/bin")

IF(WIN32)
	set(ENV{sodium_DIR} ${CMAKE_SOURCE_DIR}/libs/Sodium)
	find_package(Sodium REQUIRED)
	include_directories(${CMAKE_SOURCE_DIR}/libs/sodium/include)
	
	set(OPENSSL_ROOT_DIR ${CMAKE_SOURCE_DIR}/libs/OpenSSL/)
	find_package(OpenSSL REQUIRED)
	include_directories(${CMAKE_SOURCE_DIR}/libs/OpenSSL/)
	
	# Projects willing to statically link Sodium must define a macro named SODIUM_STATIC.
	# This will prevent symbol definitions from being referenced with __dllexport.
	# https://download.libsodium.org/doc/installation/ 
	# add_definitions(SODIUM_STATIC)
	
	
endif()

# Boost related settings: https://cmake.org/cmake/help/v3.6/module/FindBoost.html.
set(Boost_DETAILED_FAILURE_MSG on)
add_definitions(${Boost_LIB_DIAGNOSTIC_DEFINITIONS})

# Ideas for the Boost path if it is not found from any of the standard locations:
# http://stackoverflow.com/questions/29616807/how-to-change-where-cmakelists-txt-looks-for-boost-libraries-ubuntu.
# set(BOOST_ROOT C:/Program Files/boost/boost_1_63_0)
# set(BOOST_INCLUDEDIR C:/Program Files/boost/boost_1_63_0/boost)
# set(BOOST_LIBRARYDIR C:/Program Files/boost/boost_1_63_0/stage/lib)

if(NOT DEFINED BOOST_ROOT
	AND NOT DEFINED ENV{BOOST_ROOT}
	AND NOT DEFINED BOOST_INCLUDEDIR
	AND NOT DEFINED ENV{BOOST_INCLUDEDIR}
	AND NOT DEFINED BOOST_LIBRARYDIR
	AND NOT DEFINED ENV{BOOST_LIBRARYDIR})
    if(APPLE)
        # set(BOOST_ROOT "boost/boost_1_63_0/mac")
    elseif(WIN32)
        # It appears there isn't necessarily a standard install directory in Windows.
		# By default these are the ones used, though. These probably should be downloaded
		# and built on-demand...
		set(BOOST_ROOT "C:/Program Files/boost/boost_1_63_0")
		set(BOOST_INCLUDEDIR "C:/Program Files/boost/boost_1_63_0/boost")
        set(BOOST_LIBRARYDIR "C:/Program Files/boost/boost_1_63_0/stage/lib")
    endif()
endif()

if(APPLE OR WIN32)
	set(Boost_USE_STATIC_LIBS TRUE)
endif()

find_package(Boost)
message(status "** Boost Include: ${Boost_INCLUDE_DIR}")
message(status "** Boost Libraries: ${Boost_LIBRARY_DIRS}")
message(status "** Boost Libraries: ${Boost_LIBRARIES}")
IF(Boost_FOUND)
	include_directories(${Boost_INCLUDE_DIR})
endif()

# The following enables dynamic linking and multi-threading.
# Further reading at http://stackoverflow.com/questions/32252016/cmake-visual-studio-build-looks-for-wrong-library.
set(Boost_USE_STATIC_LIBS OFF)
set(Boost_USE_MULTITHREAD ON)
# target_link_libraries(some_target ${Boost_LIBRARIES})

# This sets the 'src' directory, rooted in the directory this CMakeLists.txt
# is in, as the base directory to include files.
include_directories(${CMAKE_SOURCE_DIR}/src)

# See https://crascit.com/2016/01/31/enhanced-source-file-handling-with-target_sources/
# for explanation of the following arrangment.
# Also see https://cmake.org/cmake/help/v3.7/command/add_library.html and
# http://gernotklingler.com/blog/creating-using-shared-libraries-different-compilers-different-operating-systems/.

add_library(BitcoinServer "")
add_library(BitcoinWallet "")
# add_library(EquihashTromp "")
add_library(Bitcoin "")
add_library(UnivalueBitcoin "")
add_library(BitcoinCommon "")
add_library(BitcoinUtil "")
add_library(ZCashConsensus "")
add_library(ZCash "")

include(src/CMakeLists.txt)
