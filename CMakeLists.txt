#=========================================================================
#
#  Copyright Niels Dekker, LKEB, Leiden University Medical Center
#
#  Licensed under the Apache License, Version 2.0 (the "License");
#  you may not use this file except in compliance with the License.
#  You may obtain a copy of the License at
#
#        http://www.apache.org/licenses/LICENSE-2.0.txt
#
#  Unless required by applicable law or agreed to in writing, software
#  distributed under the License is distributed on an "AS IS" BASIS,
#  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
#  See the License for the specific language governing permissions and
#  limitations under the License.
#
#=========================================================================

# Project intended to reproduce the issue that I reported at Visual Studio Developer Community
# "Visual Studio integrated CMake should define _WINDLL for a shared library"
# https://developercommunity.visualstudio.com/content/problem/1027499/visual-studio-integrated-cmake-should-define-windl.html

cmake_minimum_required( VERSION 3.16 )
project (MyProject)
message(STATUS "[${PROJECT_NAME}] CMAKE_VERSION = ${CMAKE_VERSION}")
message(STATUS "[${PROJECT_NAME}] CMAKE_GENERATOR = ${CMAKE_GENERATOR}")
set(CMAKE_VERBOSE_MAKEFILE ON)
add_library(MyDll SHARED MySource.cpp)
