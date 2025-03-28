qt_add_executable(TaskList
    WIN32 MACOSX_BUNDLE
    main.cpp
    mainwindow.cpp
    mainwindow.h
    mainwindow.ui
)

target_link_libraries(TaskList
    PRIVATE
        Qt::Core
        Qt::Widgets
)
