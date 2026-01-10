cmake_minimum_required(VERSION 4.0)

find_package(cmake-pear REQUIRED PATHS node_modules/cmake-pear)

project(pear_appling C CXX ASM)

add_pear_appling(
  pear_appling
  ID "6y6ipdm9wanepy7tcii8hu1cixwbzchskwtc9pg1czjayr7f564y"
  NAME "TracDoom"
  VERSION 0.1.0
  AUTHOR "Trac Systems UG"
  DESCRIPTION "TracDoom"

  MACOS_IDENTIFIER trac.systems.tracdoom
  MACOS_CATEGORY public.app-category.games
  MACOS_SIGNING_IDENTITY "-"

  WINDOWS_SIGNING_SUBJECT "-"
  WINDOWS_SIGNING_THUMBPRINT 0000000000000000000000000000000000000000

  LINUX_CATEGORY Game
)
