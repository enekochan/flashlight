cmake_minimum_required(VERSION 3.16)

target_sources(
  flashlight
  PRIVATE
  ${CMAKE_CURRENT_LIST_DIR}/Init.cpp
  ${CMAKE_CURRENT_LIST_DIR}/Utils.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/Activations.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/AdaptiveSoftMax.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/BatchNorm.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/Container.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/Conv2D.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/Dropout.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/Embedding.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/Identity.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/LayerNorm.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/Linear.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/Loss.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/Module.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/Normalize.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/Padding.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/PrecisionCast.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/Pool2D.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/Reorder.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/RNN.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/Transform.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/View.cpp
  ${CMAKE_CURRENT_LIST_DIR}/modules/WeightNorm.cpp
  )

if (FL_BUILD_DISTRIBUTED)
  target_sources(
    flashlight
    PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}/DistributedUtils.cpp
    )
endif()
