#[[
  SYCL Academy (c)

  SYCL Academy is licensed under a Creative Commons Attribution-ShareAlike 4.0
  International License.

  You should have received a copy of the license along with this work.  If not,
  see <http://creativecommons.org/licenses/by-sa/4.0/>.
]]

add_sycl_executable(oneMath_gemm source_onemath_usm_gemm)
add_sycl_executable(oneMath_gemm source_onemath_buffer_gemm)

target_link_libraries(oneMath_gemm_source_onemath_usm_gemm PUBLIC -lonemath)
target_link_libraries(oneMath_gemm_source_onemath_buffer_gemm PUBLIC -lonemath)
if(SYCL_ACADEMY_ENABLE_SOLUTIONS)
  add_sycl_executable(oneMath_gemm solution_onemath_usm_gemm)
  add_sycl_executable(oneMath_gemm solution_onemath_buffer_gemm)

  target_link_libraries(oneMath_gemm_solution_onemath_usm_gemm PUBLIC -lonemath)
  target_link_libraries(oneMath_gemm_solution_onemath_buffer_gemm PUBLIC -lonemath)
endif()
