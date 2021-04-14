##########################################################################
# If not stated otherwise in this file or this component's LICENSE
# file the following copyright and licenses apply:
#
# Copyright 2019 RDK Management
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
##########################################################################
include_HEADERS = $(top_srcdir)/src/xraudio_opus.h

lib_LTLIBRARIES = libxraudio-opus.la
libxraudio_opus_la_SOURCES = xraudio_opus_version.h xraudio_opus.c

BUILT_SOURCES = xraudio_opus_version.h
CLEANFILES    = xraudio_opus_version.h

xraudio_opus_version.h:
	echo "#define XRAUDIO_OPUS_VER_MAJOR \"1\"" >$@
	echo "#define XRAUDIO_OPUS_VER_MINOR \"`git -C ${srcdir} rev-list --count 4b825dc642cb6eb9a060e54bf8d69288fbee4904..HEAD``git -C ${srcdir} diff --quiet || echo \"++\"`\"" >>$@
	echo "#define XRAUDIO_OPUS_BRANCH    \"${GIT_BRANCH}\"" >>$@
	echo "#define XRAUDIO_OPUS_COMMIT_ID \"`git -C ${srcdir} log --format="%H" -n 1`\"" >>$@
	echo "#define XRAUDIO_OPUS_VERSION (XRAUDIO_OPUS_VER_MAJOR \".\" XRAUDIO_OPUS_VER_MINOR)" >>$@
