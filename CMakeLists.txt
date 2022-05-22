cmake_minimum_required(VERSION 3.22)
project(dump1090)

set(CMAKE_CXX_STANDARD 14)

include_directories(include)
add_executable(
        dump1090
        src/dump1090.c
        src/anet.c
        src/interactive.c
        src/mode_ac.c
        src/mode_s.c
        src/net_io.c
)
add_executable(
        view1090
        src/view1090.c
        src/anet.c
        src/interactive.c
        src/mode_ac.c
        src/mode_s.c
        src/net_io.c
)
target_link_libraries(dump1090 rtlsdr pthread m)
target_link_libraries(view1090 rtlsdr pthread m)