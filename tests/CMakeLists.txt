add_executable(test_placeholder test_placeholder.cpp)
target_link_libraries(test_placeholder PRIVATE ${PROJECT_NAME})
add_test(NAME placeholder COMMAND test_placeholder)