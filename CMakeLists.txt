cmake_minimum_required(VERSION 4.0)

find_package(cmake-pear REQUIRED PATHS node_modules/cmake-pear NO_DEFAULT_PATH)

project(pear_appling C CXX ASM)

if(WIN32)
  add_compile_options(-Wno-nonportable-include-path -Wno-error=nonportable-include-path)
endif()

if(APPLE)
  set(TRAC_PLATFORM_PATH "Library/Application Support/TracDoom/pear")
elseif(WIN32)
  set(TRAC_PLATFORM_PATH "TracDoom\\\\pear")
else()
  set(TRAC_PLATFORM_PATH ".config/TracDoom/pear")
endif()

add_pear_appling(
  pear_appling
  ID "6y6ipdm9wanepy7tcii8hu1cixwbzchskwtc9pg1czjayr7f564y"
  NAME "TracDoom"
  VERSION 0.1.0
  AUTHOR "Trac Systems UG"
  DESCRIPTION "TracDoom"
  WINDOWS_SIGNING_SUBJECT "CN=TracDoom Dev"
  WINDOWS_SIGNING_THUMBPRINT 4E657463CB7C1E9DF49F6703474443310AC24F39
  PLATFORM_PATH "${TRAC_PLATFORM_PATH}"

  MACOS_IDENTIFIER trac.systems.tracdoom
  MACOS_CATEGORY public.app-category.games


  LINUX_CATEGORY Game
)
