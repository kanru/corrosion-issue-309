cmake_minimum_required(VERSION 3.19.0)
project(corrosion-issue-309)

add_subdirectory(cmake/corrosion)
corrosion_import_crate(MANIFEST_PATH Cargo.toml)

add_library(rootpkg SHARED src/rootpkg.c)
target_link_libraries(rootpkg member-lib)
