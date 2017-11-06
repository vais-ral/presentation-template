#   Copyright 2017 Edoardo Pasca
#
#   Licensed under the Apache License, Version 2.0 (the "License");
#   you may not use this file except in compliance with the License.
#   You may obtain a copy of the License at
#
#       http://www.apache.org/licenses/LICENSE-2.0
#
#   Unless required by applicable law or agreed to in writing, software
#   distributed under the License is distributed on an "AS IS" BASIS,
#   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
#   See the License for the specific language governing permissions and
#   limitations under the License.

cmake_minimum_required (VERSION 3.0)

set(author "Edoardo Pasca")
set(affiliation "STFC - SCD")
set(date "07/11/2017")
set(meeting "PACE")
set(subtitle "Visual Analytics and Imaging Systems")
set(short_title "Accelerating science")
set(title "Accelerating science")
set(description "VAIS contribution to PACE: Proper Analysis of Coherent Excitations")


configure_file (${CMAKE_CURRENT_SOURCE_DIR}/index.html.in ${CMAKE_CURRENT_BINARY_DIR}/index.html)
execute_process(COMMAND ${CMAKE_COMMAND} -E copy_directory ${CMAKE_SOURCE_DIR}/css ${CMAKE_BINARY_DIR}/css)
execute_process(COMMAND ${CMAKE_COMMAND} -E copy_directory ${CMAKE_SOURCE_DIR}/img ${CMAKE_BINARY_DIR}/img)
execute_process(COMMAND ${CMAKE_COMMAND} -E copy_directory ${CMAKE_SOURCE_DIR}/js ${CMAKE_BINARY_DIR}/js)
execute_process(COMMAND ${CMAKE_COMMAND} -E copy_directory ${CMAKE_SOURCE_DIR}/plugin ${CMAKE_BINARY_DIR}/plugin)
execute_process(COMMAND ${CMAKE_COMMAND} -E copy_directory ${CMAKE_SOURCE_DIR}/lib ${CMAKE_BINARY_DIR}/lib)