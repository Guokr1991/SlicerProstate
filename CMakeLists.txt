cmake_minimum_required(VERSION 2.8.9)

project(SlicerProstate)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "http://wiki.slicer.org/slicerWiki/index.php/Documentation/Nightly/Extensions/SlicerProstate")
set(EXTENSION_CATEGORY "Applications")
set(EXTENSION_CONTRIBUTORS "Andrey Fedorov (Brigham and Women's Hospital), Andras Lasso (Queen's University)")
set(EXTENSION_DESCRIPTION "SlicerProstate extension hosts various modules to facilitate processing and management of prostate image data, utilizing prostate images in image-guided interventions and development of the imaging biomarkers of the prostate cancer.")
set(EXTENSION_ICONURL "http://wiki.slicer.org/slicerWiki/images/8/87/SlicerProstate_Logo_1.0_128x128.png")
set(EXTENSION_SCREENSHOTURLS "http://wiki.slicer.org/slicerWiki/images/f/ff/DistanceMapBasedRegistration_example1.png http://wiki.slicer.org/slicerWiki/images/3/36/SegmentationSmoothing_example1.png http://wiki.slicer.org/slicerWiki/images/c/c3/QuadEdgeSurfaceMesher_example1.png")

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(QuadEdgeSurfaceMesher)
add_subdirectory(SegmentationSmoothing)
add_subdirectory(DistanceMapBasedRegistration)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_CPACK})
