cmake_minimum_required(VERSION 3.20.0)

# TODO LLM: the following lines should not be needed, as the zenbedded module should be automatically detected
# list(APPEND ZEPHYR_EXTRA_MODULES
#     "${CMAKE_CURRENT_LIST_DIR}/../../../zenbedded_transport"
#     "${CMAKE_CURRENT_LIST_DIR}/../../../zenbedded_rcl"
# )

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})

project(zenbedded_demo_tier1)
target_sources(app PRIVATE src/main.cpp)