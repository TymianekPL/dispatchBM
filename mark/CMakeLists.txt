add_executable(mark)

target_sources(mark PRIVATE src/main.cpp)
target_link_libraries(mark PRIVATE bench)
