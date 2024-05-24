set(HEADERS c99_compat.h
    no_extern_c.h
    threads.h
    threads_posix.h
    threads_win32.h)

configure_file(${CMAKE_CURRENT_SOURCE_DIR}/c11.conf.h.cmake
               ${CMAKE_CURRENT_BINARY_DIR}/c11.conf.h)

install(FILES ${HEADERS} ${CMAKE_CURRENT_BINARY_DIR}/c11.conf.h
    DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}/c11emu/header_only)
