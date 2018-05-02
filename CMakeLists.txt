cmake_minimum_required(VERSION 2.8)
project( mono-vo )
find_package( OpenCV 3.0 REQUIRED )

include_directories( ${OpenCV_INCLUDE_DIRS} )

file(GLOB viso
    "src/visodo.h"
    "src/visodo_video.cpp"
)
add_executable( vo_video ${viso} )
target_link_libraries( vo_video ${OpenCV_LIBS} )
