add_library(LIB_DLDB_BERT 
    he.cpp
    nonlinear.cpp
    linear.cpp
    bert_utils.cpp
    bert.cpp
    )

target_link_libraries(LIB_DLDB_BERT SCI-FloatingPoint)
target_link_libraries(LIB_DLDB_BERT SCI-HE)

# add_executable(BERT_NONLINEAR "test_nonlinear.cpp")
# target_link_libraries(BERT_NONLINEAR NONLINEAR)

add_executable(DLDB_BERT "dldb_bert.cpp")
target_link_libraries(DLDB_BERT LIB_DLDB_BERT)


# add_executable(BOLT_WE_BERT "bolt_bert_word_elimination.cpp")
# target_link_libraries(BOLT_WE_BERT LIB_BERT)
