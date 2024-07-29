cmake_minimum_required(VERSION 3.10)

project(ImGuizmo VERSION 1.84.0 DESCRIPTION "Immediate mode 3D gizmo for scene editing and other controls based on Dear Imgui.")

include(GNUInstallDirs)

add_library(ImGuizmo
        GraphEditor.cpp
        GraphEditor.h
        ImCurveEdit.cpp
        ImCurveEdit.h
        ImGradient.cpp
        ImGradient.h
        ImGuizmo.cpp
        ImGuizmo.h
        ImSequencer.cpp
        ImSequencer.h
        ImZoomSlider.h
)


set_target_properties(ImGuizmo PROPERTIES VERSION ${PROJECT_VERSION})
set_target_properties(ImGuizmo PROPERTIES SOVERSION 1)

target_include_directories(ImGuizmo PUBLIC .)

set_property(TARGET ImGuizmo PROPERTY POSITION_INDEPENDENT_CODE ON)
