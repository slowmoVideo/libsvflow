# Static libraries
# http://www.itk.org/pipermail/insight-users/2007-November/024141.html
# http://www.linux-magazin.de/Heft-Abo/Ausgaben/2007/02/Mal-ausspannen

project(libsvflow)

set(LIB_SRC_FLOW
  src/flowRW_sV.cpp
  src/flowField_sV.cpp
)
set(HEADERS
  src/flowRW_sV.h
  src/flowField_sV.h
)


add_library(sVflow  STATIC ${LIB_SRC_FLOW})