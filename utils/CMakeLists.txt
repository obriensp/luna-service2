# @@@LICENSE
#
#      Copyright (c) 2008-2012 Hewlett-Packard Development Company, L.P.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
# LICENSE@@@

#
# luna-service2/utils/CMakeLists.txt
#

#
# The *.sh scripts in this directory are intentionally not installed.
#

add_executable(luna-helper luna-helper.c)
target_link_libraries(luna-helper ${LS2_LIBRARY_NAME})

add_executable(luna-send luna-send.c)
target_link_libraries(luna-send ${LS2_LIBRARY_NAME})

install(TARGETS luna-helper DESTINATION bin ${RESTRICTED_PERMS})
install(TARGETS luna-send DESTINATION bin ${RESTRICTED_PERMS})
install(PROGRAMS ls-control DESTINATION bin ${RESTRICTED_PERMS})
