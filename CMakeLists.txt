cmake_minimum_required(VERSION 2.6.2)

project(wwxFoldbar)

find_package(wxWidgets COMPONENTS core base adv REQUIRED)
include( ${wxWidgets_USE_FILE} )

include_directories("include")

add_library(wxFoldbar SHARED
	src/captionbar.cpp
	src/foldpanelbar.cpp
	src/foldpanelitem.cpp
)

target_link_libraries(wxFoldbar ${wxWidgets_LIBRARIES})

#add_executable(demo
#	samples/foldpanelbar/foldpanelbartest.cpp
#	samples/foldpanelbar/foldtestpanel.cpp
#	samples/foldpanelbar/layouttest.cpp
#	samples/foldpanelbar/test.cpp
#)

#add_executable(extended
#	samples/extended/extended.cpp
#)

#target_link_libraries(demo wxFoldbar)
#target_link_libraries(extended wxFoldbar)
