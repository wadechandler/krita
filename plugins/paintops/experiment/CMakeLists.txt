set(kritaexperimentpaintop_SOURCES
    experiment_paintop_plugin.cpp
    kis_experiment_paintop.cpp
    kis_experiment_paintop_settings.cpp
    kis_experiment_paintop_settings_widget.cpp
    KisExperimentOpOptionData.cpp
    KisExperimentOpOptionModel.cpp
    KisExperimentOpOptionWidget.cpp
    
    )

ki18n_wrap_ui(kritaexperimentpaintop_SOURCES wdgexperimentoptions.ui )

kis_add_library(kritaexperimentpaintop MODULE ${kritaexperimentpaintop_SOURCES})

target_link_libraries(kritaexperimentpaintop kritalibpaintop)

install(TARGETS kritaexperimentpaintop  DESTINATION ${KRITA_PLUGIN_INSTALL_DIR})
install( FILES
    krita-experiment.png DESTINATION ${KDE_INSTALL_DATADIR}/krita/images)


