# Headers
set(mvsUtils_files_headers
  common.hpp
  fileIO.hpp
  ImagesCache.hpp
  MultiViewParams.hpp
  PreMatchCams.hpp
)

# Sources
set(mvsUtils_files_sources
  common.cpp
  fileIO.cpp
  ImagesCache.cpp
  MultiViewParams.cpp
  PreMatchCams.cpp
)

alicevision_add_library(aliceVision_mvsUtils
  SOURCES ${mvsUtils_files_headers} ${mvsUtils_files_sources}
  PUBLIC_LINKS
    aliceVision_mvsData
    aliceVision_imageIO
  PRIVATE_LINKS
    aliceVision_system
    ${Boost_FILESYSTEM_LIBRARY}
)
