file(GLOB HEADER_FILES *.h)
add_library(n64 STATIC endgameSearch.cpp endgameSearchTest.cpp flips.cpp flipsTest.cpp hash.cpp hashTest.cpp lastFlipCountGenerator.cpp magic.cpp n64.cpp solve.cpp solveTest.cpp stdafx.cpp test.cpp utils.cpp utilsTest.cpp bitExtractTest.cpp ${HEADER_FILES})

add_executable(bitExtractTest bitExtractTestMain.cpp)
target_link_libraries(bitExtractTest n64)


add_test(bitExtract bitExtractTest)
