# CMakeList.txt: проект CMake для MyThreadPool; включите исходный код и определения,
# укажите здесь логику для конкретного проекта.
#

# Добавьте источник в исполняемый файл этого проекта.
add_executable (MyThreadPool "main.cpp" "include/MyThreadPool.h" "src/MyThreadPool.cpp")

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET MyThreadPool PROPERTY CXX_STANDARD 20)
endif()

target_include_directories(
	MyThreadPool PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include 
	MyThreadPool PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src
)

# TODO: Добавьте тесты и целевые объекты, если это необходимо.
