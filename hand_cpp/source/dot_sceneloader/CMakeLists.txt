INCLUDE_DIRECTORIES(tinyxml)
ADD_SUBDIRECTORY(tinyxml)

ADD_LIBRARY(dot_sceneloader STATIC dot_sceneloader.cc)
TARGET_LINK_LIBRARIES(dot_sceneloader tinyxml)

INSTALL(TARGETS dot_sceneloader EXPORT LibHand-export DESTINATION ${HAND_LIB_DIST_DIR})
