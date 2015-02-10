fips_begin_lib(polyvox)
	include_directories(polyvox/library/PolyVoxCore/include polyvox/library/PolyVoxCore/include/PolyVoxCore polyvox/library/PolyVoxCore/include/PolyVoxCore/Impl)
	fips_files(
		polyvox/library/PolyVoxCore/source/MeshDecimator.cpp
		polyvox/library/PolyVoxCore/source/Impl/RandomVectors.cpp
		polyvox/library/PolyVoxCore/source/Impl/Utility.cpp
		polyvox/library/PolyVoxCore/source/Impl/RandomUnitVectors.cpp
		polyvox/library/PolyVoxCore/source/Impl/MarchingCubesTables.cpp
		polyvox/library/PolyVoxCore/source/AStarPathfinder.cpp
		polyvox/library/PolyVoxCore/source/ArraySizes.cpp
		polyvox/library/PolyVoxCore/source/VertexTypes.cpp
		polyvox/library/PolyVoxCore/source/Region.cpp
		polyvox/library/PolyVoxCore/source/SimpleInterface.cpp
		polyvox/library/PolyVoxCore/source/Log.cpp
	)
	# hack to silence some warnings
	#if (FIPS_MACOS)
	#	set_target_properties(polyvox PROPERTIES COMPILE_FLAGS "-Wno-sign-compare -Wno-deprecated-declarations")
	#elseif(FIPS_LINUX)
	#	set_target_properties(polyvox PROPERTIES COMPILE_FLAGS "-Wno-sign-compare")
	#endif()
fips_end_lib()
