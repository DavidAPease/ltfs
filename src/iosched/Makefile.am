#
#
#  OO_Copyright_BEGIN
#
#
#  Copyright 2010, 2017 IBM Corp.
#
#  Redistribution and use in source and binary forms, with or without
#   modification, are permitted provided that the following conditions
#  are met:
#  1. Redistributions of source code must retain the above copyright
#     notice, this list of conditions and the following disclaimer.
#  2. Redistributions in binary form must reproduce the above copyright
#     notice, this list of conditions and the following disclaimer in the
#  documentation and/or other materials provided with the distribution.
#  3. Neither the name of the copyright holder nor the names of its
#     contributors may be used to endorse or promote products derived from
#     this software without specific prior written permission.
#
#  THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS ``AS IS''
#  AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
#  IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
#  ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE
#  LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
#  CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF
#  SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS
#  INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN
#  CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)
#  ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
#  POSSIBILITY OF SUCH DAMAGE.
#
#
#  OO_Copyright_END
#

lib_LTLIBRARIES = libiosched-fcfs.la libiosched-unified.la
libdir = @libdir@/ltfs

AM_LIBTOOLFLAGS = --tag=disable-static

libiosched_fcfs_la_SOURCES = fcfs.c
libiosched_fcfs_la_LDFLAGS = -avoid-version -module @AM_LDFLAGS@
libiosched_fcfs_la_DEPENDENCIES = ../../messages/iosched_fcfs_dat.o
libiosched_fcfs_la_LIBADD = ../../messages/iosched_fcfs_dat.o
libiosched_fcfs_la_CPPFLAGS = @AM_CPPFLAGS@ -I ..

libiosched_unified_la_SOURCES = unified.c cache_manager.c
libiosched_unified_la_LDFLAGS = -avoid-version -module @AM_LDFLAGS@
libiosched_unified_la_DEPENDENCIES = ../../messages/iosched_unified_dat.o
libiosched_unified_la_LIBADD = ../../messages/iosched_unified_dat.o
libiosched_unified_la_CPPFLAGS = @AM_CPPFLAGS@ -I ..

install-exec-hook:
	for f in $(lib_LTLIBRARIES); do rm -f $(libdir)/$$f; done
