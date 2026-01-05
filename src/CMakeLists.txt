file(GLOB_RECURSE CPP_SRC_FILES ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)

add_library(eidolon ${CPP_SRC_FILES})

target_link_libraries(eidolon
  PUBLIC math
  PUBLIC bvh
  PUBLIC stb_cmake
  PUBLIC glfw
  PUBLIC volk
  PUBLIC vk-bootstrap
  PUBLIC VulkanMemoryAllocator
  PUBLIC slang
  PUBLIC imgui_cmake
  PUBLIC model
)

target_include_directories(eidolon
  PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/../includes
  PUBLIC slang
  PUBLIC vk-bootstrap
)