# SPDX-License-Identifier: Apache-2.0

if(CONFIG_STM32_EXTERNAL_DRIVERS)
  zephyr_include_directories(include)

  add_subdirectory(drivers)
  add_subdirectory_ifdef(CONFIG_EXTERNAL_APPS apps)
  add_subdirectory_ifdef(CONFIG_EXTERNAL_MATH math)
  add_subdirectory(subsys)

endif()
