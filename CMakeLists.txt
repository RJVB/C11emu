cmake_minimum_required(VERSION 3.0)

project(c11emu
    VERSION 1.0
    DESCRIPTION "Emulation of the C11 Concurrency Support Library")

include(CheckSymbolExists)
include(GNUInstallDirs)
include(FeatureSummary)

check_symbol_exists(timespec_get "time.h" HAVE_TIMESPEC_GET)

add_subdirectory(header_only)

feature_summary(WHAT ALL   FATAL_ON_MISSING_REQUIRED_PACKAGES)
