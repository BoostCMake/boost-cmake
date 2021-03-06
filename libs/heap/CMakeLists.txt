cmake_minimum_required(VERSION 3.5)

find_package(CM)
include(CMDeploy)
include(CMSetupVersion)

cm_project(${CMAKE_WORKSPACE_NAME} heap)

find_package(${CMAKE_WORKSPACE_NAME}_static_assert)
find_package(${CMAKE_WORKSPACE_NAME}_iterator)
find_package(${CMAKE_WORKSPACE_NAME}_bind)
find_package(${CMAKE_WORKSPACE_NAME}_mpl)
find_package(${CMAKE_WORKSPACE_NAME}_intrusive)
find_package(${CMAKE_WORKSPACE_NAME}_assert)
find_package(${CMAKE_WORKSPACE_NAME}_type_traits)
find_package(${CMAKE_WORKSPACE_NAME}_concept_check)
find_package(${CMAKE_WORKSPACE_NAME}_array)
find_package(${CMAKE_WORKSPACE_NAME}_config)
find_package(${CMAKE_WORKSPACE_NAME}_parameter)
find_package(${CMAKE_WORKSPACE_NAME}_throw_exception)

cm_setup_version(VERSION 1.60.0)

add_library(${CMAKE_WORKSPACE_NAME}_${CURRENT_PROJECT_NAME} INTERFACE)
set_property(TARGET ${CMAKE_WORKSPACE_NAME}_${CURRENT_PROJECT_NAME} PROPERTY EXPORT_NAME heap)

target_link_libraries(${CMAKE_WORKSPACE_NAME}_${CURRENT_PROJECT_NAME} INTERFACE ${CMAKE_WORKSPACE_NAME}::static_assert)
target_link_libraries(${CMAKE_WORKSPACE_NAME}_${CURRENT_PROJECT_NAME} INTERFACE ${CMAKE_WORKSPACE_NAME}::iterator)
target_link_libraries(${CMAKE_WORKSPACE_NAME}_${CURRENT_PROJECT_NAME} INTERFACE ${CMAKE_WORKSPACE_NAME}::bind)
target_link_libraries(${CMAKE_WORKSPACE_NAME}_${CURRENT_PROJECT_NAME} INTERFACE ${CMAKE_WORKSPACE_NAME}::mpl)
target_link_libraries(${CMAKE_WORKSPACE_NAME}_${CURRENT_PROJECT_NAME} INTERFACE ${CMAKE_WORKSPACE_NAME}::intrusive)
target_link_libraries(${CMAKE_WORKSPACE_NAME}_${CURRENT_PROJECT_NAME} INTERFACE ${CMAKE_WORKSPACE_NAME}::assert)
target_link_libraries(${CMAKE_WORKSPACE_NAME}_${CURRENT_PROJECT_NAME} INTERFACE ${CMAKE_WORKSPACE_NAME}::type_traits)
target_link_libraries(${CMAKE_WORKSPACE_NAME}_${CURRENT_PROJECT_NAME} INTERFACE ${CMAKE_WORKSPACE_NAME}::concept_check)
target_link_libraries(${CMAKE_WORKSPACE_NAME}_${CURRENT_PROJECT_NAME} INTERFACE ${CMAKE_WORKSPACE_NAME}::array)
target_link_libraries(${CMAKE_WORKSPACE_NAME}_${CURRENT_PROJECT_NAME} INTERFACE ${CMAKE_WORKSPACE_NAME}::config)
target_link_libraries(${CMAKE_WORKSPACE_NAME}_${CURRENT_PROJECT_NAME} INTERFACE ${CMAKE_WORKSPACE_NAME}::parameter)
target_link_libraries(${CMAKE_WORKSPACE_NAME}_${CURRENT_PROJECT_NAME} INTERFACE ${CMAKE_WORKSPACE_NAME}::throw_exception)

cm_deploy(TARGETS ${CMAKE_WORKSPACE_NAME}_${CURRENT_PROJECT_NAME} INCLUDE ${CURRENT_SOURCES_DIR}/include NAMESPACE ${CMAKE_WORKSPACE_NAME}::)

add_subdirectory(test)
