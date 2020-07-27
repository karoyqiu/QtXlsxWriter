cmake_minimum_required(VERSION 3.0)

project(QtXlsx)
add_subdirectory("src/xlsx")

#####
#
# Installation configuration
#
#####
install(TARGETS QtXlsx
  RUNTIME DESTINATION bin
  LIBRARY DESTINATION lib${LIB_SUFFIX}
  ARCHIVE DESTINATION lib${LIB_SUFFIX}
)

#INSTALL(FILES  ${CMAKE_CURRENT_BINARY_DIR}/QtXlsxWriterConfig.cmake DESTINATION
#    lib${LIB_SUFFIX}/cmake/${PROJECT_NAME})

SET(INCLUDE_FILES
  src/xlsx/xlsxabstractooxmlfile.h
  src/xlsx/xlsxabstractsheet.h
  src/xlsx/xlsxcell.h
  src/xlsx/xlsxcellformula.h
  src/xlsx/xlsxcellrange.h
  src/xlsx/xlsxcellreference.h
  src/xlsx/xlsxchart.h
  src/xlsx/xlsxchartsheet.h
  src/xlsx/xlsxconditionalformatting.h
  src/xlsx/xlsxdatavalidation.h
  src/xlsx/xlsxdocument.h
  src/xlsx/xlsxformat.h
  src/xlsx/xlsxglobal.h
  src/xlsx/xlsxrichstring.h
  src/xlsx/xlsxworkbook.h
  src/xlsx/xlsxworksheet.h
)
install(FILES ${INCLUDE_FILES} DESTINATION include)
