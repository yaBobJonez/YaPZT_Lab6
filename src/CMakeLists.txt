qt_add_executable(YaPZT_Lab6
    WIN32 MACOSX_BUNDLE
    main.cpp
    mainwindow.cpp
    mainwindow.h
    mainwindow.ui
)

target_link_libraries(YaPZT_Lab6
    PRIVATE
        Qt::Core
        Qt::Widgets
)
