# ##############################################################################
# apps/system/perf-tools/CMakeLists.txt
#
# Licensed to the Apache Software Foundation (ASF) under one or more contributor
# license agreements.  See the NOTICE file distributed with this work for
# additional information regarding copyright ownership.  The ASF licenses this
# file to you under the Apache License, Version 2.0 (the "License"); you may not
# use this file except in compliance with the License.  You may obtain a copy of
# the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
# WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  See the
# License for the specific language governing permissions and limitations under
# the License.
#
# ##############################################################################

if(CONFIG_PERF_TOOLS)
  nuttx_add_application(
    MODULE
    ${CONFIG_PERF_TOOLS}
    NAME
    perf
    STACKSIZE
    ${CONFIG_PERF_TOOLS_STACKSIZE}
    PRIORITY
    ${CONFIG_PERF_TOOLS_PRIORITY}
    SRCS
    perf.c
    builtin-help.c
    builtin-list.c
    builtin-record.c
    builtin-stat.c
    builtin-version.c
    builtin-write.c
    evlist.c
    evsel.c
    parse-options.c)
endif()
