
ion_src += $(addprefix ion/src/simulator/3ds/, \
  main.cpp \
  callback.cpp \
  clipboard.cpp \
  display.cpp \
  framebuffer.cpp \
  telemetry_init.cpp \
  keyboard.cpp \
  events_keyboard.cpp \
  events.cpp \
  driver/display.cpp \
  driver/language.cpp \
  driver/led.cpp \
  driver/usb.cpp \
  driver/battery.cpp \
  driver/common.cpp \
)

ion_src += ion/src/shared/collect_registers.cpp

sdl_simu_needs_to_be_removed += $(addprefix ion/src/shared/, \
  dummy/display.cpp \
  dummy/led.cpp \
  dummy/usb.cpp \
  dummy/battery.cpp \
  dummy/store_script.cpp \
)

sdl_simu_needs_to_be_removed += $(addprefix ion/src/simulator/shared/, \
  clipboard.cpp \
  display.cpp:-headless \
  events_keyboard.cpp:-headless \
  events.cpp \
  events_platform.cpp \
  framebuffer_base.cpp \
  framebuffer.cpp \
  keyboard_sdl.cpp:-headless \
  keyboard.cpp \
  main_sdl.cpp:-headless \
  main.cpp \
  layout.cpp:-headless \
  timing.cpp \
)

# Remove the dummy display (re-implemented) and the SDL simulator stuff.
ion_src := $(filter-out $(sdl_simu_needs_to_be_removed),$(ion_src))
