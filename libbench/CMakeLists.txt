add_library(bench STATIC)

target_sources(bench PUBLIC FILE_SET CXX_MODULES FILES
     src/bench.ixx
)
