cmake_minimum_required(VERSION 3.17)
project(PasswordCracking LANGUAGES C CXX CUDA)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CUDA_STANDARD 14)

add_executable(PasswordCracking src/main.cu
        src/md5.c)

set_target_properties(PasswordCracking PROPERTIES
        CUDA_SEPARABLE_COMPILATION ON CUDA_ARCHITECTURES "native")