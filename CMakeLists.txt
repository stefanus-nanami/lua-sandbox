cmake_minimum_required(VERSION 3.10)

# set the project name
project(lua-sandbox)

# add the executable
add_executable(lua-sandbox src/lua-sandbox.cpp)

target_compile_features(lua-sandbox PRIVATE cxx_std_17)

target_link_libraries(lua-sandbox PUBLIC
                      ${lua-sandbox_SOURCE_DIR}/lib/liblua.a
                      ${CMAKE_DL_LIBS}
                      pthread)

target_include_directories(lua-sandbox PUBLIC
                          "${lua-sandbox_SOURCE_DIR}/include"
                          "${lua-sandbox_SOURCE_DIR}/include/asio")
