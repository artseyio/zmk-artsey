#
# Copyright (c) 2021 Mike "KemoNine" Crosson
# SPDX-License-Identifier: MIT
#

target_sources_ifdef(CONFIG_SHIELD_BLUEHAND_LEFT || CONFIG_SHIELD_BLUEHAND_RIGHT app PRIVATE pwr_led.c)
