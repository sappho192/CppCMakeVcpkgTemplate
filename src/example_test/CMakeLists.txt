project(example_test)

add_executable(example_test test.cpp)

find_package(unofficial-sqlite3 CONFIG REQUIRED)
target_link_libraries(example_test PRIVATE unofficial::sqlite3::sqlite3 fmt::fmt-header-only)
set_property(TARGET example_test PROPERTY CXX_STANDARD 23)

add_test(example_test example_test)