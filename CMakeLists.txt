cmake_minimum_required(VERSION 2.8)
Project(svmlight C)

set(CMAKE_BUILD_TYPE Release) 
set(INCLUDE  ${CMAKE_CURRENT_SOURCE_DIR})


add_library(svmlight SHARED svm_classify.c svm_common.c svm_learn.c svm_hideo.c)

install(TARGETS svmlight DESTINATION /usr/local/lib)
install(FILES svm_common.h svm_learn.h DESTINATION /usr/local/include)