cmake_minimum_required(VERSION 2.8.12)


##################################################
## Project
##################################################
project(crunch)

set(SOURCE_CODES
	crnlib/crn_arealist.cpp 
	crnlib/crn_assert.cpp 
	crnlib/crn_checksum.cpp 
	crnlib/crn_colorized_console.cpp 
	crnlib/crn_command_line_params.cpp 
	crnlib/crn_comp.cpp 
	crnlib/crn_console.cpp 
	crnlib/crn_core.cpp 
	crnlib/crn_data_stream.cpp 
	crnlib/crn_mipmapped_texture.cpp 
	crnlib/crn_decomp.cpp 
	crnlib/crn_dxt1.cpp 
	crnlib/crn_dxt5a.cpp 
	crnlib/crn_dxt.cpp 
	crnlib/crn_dxt_endpoint_refiner.cpp 
	crnlib/crn_dxt_fast.cpp 
	crnlib/crn_dxt_hc_common.cpp 
	crnlib/crn_dxt_hc.cpp 
	crnlib/crn_dxt_image.cpp 
	crnlib/crn_dynamic_string.cpp 
	crnlib/crn_file_utils.cpp 
	crnlib/crn_find_files.cpp 
	crnlib/crn_hash.cpp 
	crnlib/crn_hash_map.cpp 
	crnlib/crn_huffman_codes.cpp 
	crnlib/crn_image_utils.cpp 
	crnlib/crnlib.cpp 
	crnlib/crn_math.cpp 
	crnlib/crn_mem.cpp 
	crnlib/crn_pixel_format.cpp 
	crnlib/crn_platform.cpp 
	crnlib/crn_prefix_coding.cpp 
	crnlib/crn_qdxt1.cpp 
	crnlib/crn_qdxt5.cpp 
	crnlib/crn_rand.cpp 
	crnlib/crn_resample_filters.cpp 
	crnlib/crn_resampler.cpp 
	crnlib/crn_ryg_dxt.cpp 
	crnlib/crn_sparse_bit_array.cpp 
	crnlib/crn_stb_image.cpp 
	crnlib/crn_strutils.cpp 
	crnlib/crn_symbol_codec.cpp 
	crnlib/crn_texture_file_types.cpp 
	crnlib/crn_threaded_resampler.cpp 
	crnlib/crn_threading_pthreads.cpp 
	crnlib/crn_timer.cpp 
	crnlib/crn_utils.cpp 
	crnlib/crn_value.cpp 
	crnlib/crn_vector.cpp 
	crnlib/crn_zeng.cpp 
	crnlib/crn_texture_comp.cpp 
	crnlib/crn_texture_conversion.cpp 
	crnlib/crn_dds_comp.cpp 
	crnlib/crn_lzma_codec.cpp 
	crnlib/crn_ktx_texture.cpp 
	crnlib/crn_etc.cpp 
	crnlib/crn_rg_etc1.cpp 
	crnlib/crn_miniz.cpp 
	crnlib/crn_jpge.cpp 
	crnlib/crn_jpgd.cpp 
	crnlib/lzma_7zBuf2.cpp 
	crnlib/lzma_7zBuf.cpp 
	crnlib/lzma_7zCrc.cpp 
	crnlib/lzma_7zFile.cpp 
	crnlib/lzma_7zStream.cpp 
	crnlib/lzma_Alloc.cpp 
	crnlib/lzma_Bcj2.cpp 
	crnlib/lzma_Bra86.cpp 
	crnlib/lzma_Bra.cpp 
	crnlib/lzma_BraIA64.cpp 
	crnlib/lzma_LzFind.cpp 
	crnlib/lzma_LzmaDec.cpp 
	crnlib/lzma_LzmaEnc.cpp 
	crnlib/lzma_LzmaLib.cpp
)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ")

add_library(crunch STATIC ${SOURCE_CODES})
target_compile_options(crunch PRIVATE -O3 -fPIC -fomit-frame-pointer -ffast-math -fno-math-errno -fno-strict-aliasing -Wall)
target_compile_options(crunch PRIVATE -Wno-unused-value -Wno-unused -Wno-unused-value -Wno-unused -Wno-misleading-indentation)
