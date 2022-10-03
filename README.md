BOARD=esp8266-esp-12x podman container runlabel run ghcr.io/burgrp/riot-esp8266 make flash

BOARD=esp32-wroom-32 podman container runlabel run ghcr.io/burgrp/riot-esp32 make clean flash

BOARD=samd10-xmini podman container runlabel run ghcr.io/burgrp/riot-arm make flash
