#
# Copyright 2018 Staysail Systems, Inc. <info@staysail.tech>
# Copyright 2018 Capitar IT Group BV <info@capitar.com>
#
# This software is supplied under the terms of the MIT License, a
# copy of which should be located in the distribution where this
# file was obtained (LICENSE.txt).  A copy of the license may also be
# found online at https://opensource.org/licenses/MIT.
#

# ipc protocol
option (NNG_TRANSPORT_IPC "Enable IPC transport." ON)
mark_as_advanced(NNG_TRANSPORT_IPC)

if (NNG_TRANSPORT_IPC)
    set(_DEFS -DNNG_TRANSPORT_IPC)
    set(_SRCS transport/ipc/ipc.c ${PROJECT_SOURCE_DIR}/include/nng/transport/ipc/ipc.h)

    set(NNG_DEFS ${NNG_DEFS} ${_DEFS} PARENT_SCOPE)
    set(NNG_SRCS ${NNG_SRCS} ${_SRCS} PARENT_SCOPE)
endif()
