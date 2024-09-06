project(example_app)

add_executable(main main.cpp)

find_package(unofficial-sqlite3 CONFIG REQUIRED)
target_link_libraries(main PRIVATE unofficial::sqlite3::sqlite3 fmt::fmt-header-only)

set_property(TARGET main PROPERTY CXX_STANDARD 23)
