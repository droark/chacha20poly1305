CMAKE_MINIMUM_REQUIRED( VERSION 3.3 )

SET( CHACHA20POLY1305_LIB_NAME  libchacha20poly1305 )
PROJECT( ${CHACHA20POLY1305_LIB_NAME} )

FILE(GLOB SOURCES *.c)
list(REMOVE_ITEM SOURCES ${CMAKE_CURRENT_SOURCE_DIR}/tests.c)

FILE(GLOB HEADERS *.h)

ADD_LIBRARY( ${CHACHA20POLY1305_LIB_NAME} ${SOURCES} ${HEADERS})
TARGET_LINK_LIBRARIES(${CHACHA20POLY1305_LIB_NAME})
