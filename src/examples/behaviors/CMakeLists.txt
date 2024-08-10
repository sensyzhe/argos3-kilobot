if(ARGOS_BUILD_FOR_SIMULATOR)
  include_directories(${CMAKE_SOURCE_DIR}/argos3/plugins/robots/kilobot/control_interface)

add_executable(agentCDCIlocal_compare agentCDCIlocal.h agentCDCIlocal_compare.c)
if(UNIX AND NOT APPLE)
	target_link_libraries(agentCDCIlocal_compare  argos3plugin_simulator_kilolib rt m) 
else(UNIX AND NOT APPLE)
	target_link_libraries(agentCDCIlocal_compare  argos3plugin_simulator_kilolib) 
endif()

add_executable(agentCDCIlocal_resample agentCDCIlocal.h agentCDCIlocal_resample.c)
if(UNIX AND NOT APPLE)
	target_link_libraries(agentCDCIlocal_resample  argos3plugin_simulator_kilolib rt m) 
else(UNIX AND NOT APPLE)
	target_link_libraries(agentCDCIlocal_resample  argos3plugin_simulator_kilolib) 
endif()

endif(ARGOS_BUILD_FOR_SIMULATOR)
