add_library(jet_vector SHARED jet_vector.cpp)
cuda_add_library(jet_vector_CUDA SHARED jet_vector.cu)

add_library(jet_vector_math_impl_CPU SHARED jet_vector_math_impl.cpp)
cuda_add_library(jet_vector_math_impl_CUDA SHARED jet_vector_math_impl.cu)

target_link_libraries(jet_vector jet_vector_CUDA jet_vector_math_impl_CPU jet_vector_math_impl_CUDA)
