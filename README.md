# SDL 2.26 bindings for Odin
Based on `vendor:sdl2` (which is SDL 2.0.16) and updated to 2.26.x 

## How to work on this
Go to this diff: https://github.com/libsdl-org/SDL/compare/release-2.0.16...release-2.26.2?diff=split

run this to collapse all diffs (may take a few seconds):
`document.querySelectorAll('button[aria-label="Toggle diff contents"][aria-expanded=true]').forEach(b=>b.click())`

Search for all files with path "include/", these are the files that need checking.

## Progress
Here is a list of all header files from SDL 2.26 that need to be looked at

- [x] begin_code.h (C craziness. No need w/ Odin)
- [x] close_code.h (C craziness. No need w/ Odin)
- [x] SDL.h
- [x] SDL_assert.h (C craziness. No need w/ Odin)
- [x] SDL_atomic.h
- [x] SDL_audio.h
- [x] SDL_bits.h
- [x] SDL_blendmode.h
- [x] SDL_clipboard.h
- [x] SDL_config.h (All config headers are C craziness. No need w/ Odin)
  - [x] SDL_config.h.in
  - [x] SDL_config_android.h
  - [x] SDL_config_emscripten.h
  - [x] SDL_config_iphoneos.h
  - [x] SDL_config_macosx.h
  - [x] SDL_config_minimal.h
  - [x] SDL_config_ngage.h
  - [x] SDL_config_os2.h
  - [x] SDL_config_pandora.h
  - [x] SDL_config_windows.h
  - [x] SDL_config_wingdk.h
  - [x] SDL_config_winrt.h
  - [x] SDL_config_xbox.h
- [x] SDL_copying.h (literally just the copyright disclaimer thats already at the top of every file)
- [x] SDL_cpuinfo.h
- [x] SDL_egl.h (C craziness. No need w/ Odin)
- [x] SDL_endian.h (stuff that's in core:encoding/endian)
- [x] SDL_error.h
- [x] SDL_events.h
- [x] SDL_filesystem.h
- [x] SDL_gamecontroller.h
- [x] SDL_gesture.h
- [x] SDL_guid.h
- [x] SDL_haptic.h
- [x] SDL_hidapi.h
- [x] SDL_hints.h
- [x] SDL_joystick.h
- [x] SDL_keyboard.h
- [x] SDL_keycode.h
- [x] SDL_loadso.h
- [x] SDL_locale.h
- [x] SDL_log.h
- [ ] SDL_main.h (none of the things in here are in the original odin bindings, so I'll skip the things that got added here too for now)
- [x] SDL_messagebox.h
- [x] SDL_metal.h
- [x] SDL_misc.h
- [x] SDL_mouse.h
- [x] SDL_mutex.h
- [x] SDL_name.h
- [ ] SDL_opengl.h (most of this stuff is in vendor:OpenGL, though not all of it. I'm skipping this because the original odin bindings also skipped it)
  - [ ] SDL_opengl_glext.h
  - [ ] SDL_opengles.h
  - [ ] SDL_opengles2.h
  - [ ] SDL_opengles2_gl2.h
  - [ ] SDL_opengles2_gl2ext.h
  - [ ] SDL_opengles2_gl2platform.h
  - [ ] SDL_opengles2_khrplatform.h
- [x] SDL_pixels.h
- [x] SDL_platform.h
- [x] SDL_power.h
- [x] SDL_quit.h
- [x] SDL_rect.h
- [x] SDL_render.h
- [x] SDL_revision.h
- [x] SDL_rwops.h
- [x] SDL_scancode.h
- [x] SDL_sensor.h
- [x] SDL_shape.h
- [ ] SDL_stdinc.h
- [ ] SDL_surface.h
- [ ] SDL_system.h
- [ ] SDL_syswm.h
- [ ] SDL_test.h
  - [ ] SDL_test_assert.h
  - [ ] SDL_test_common.h
  - [ ] SDL_test_compare.h
  - [ ] SDL_test_crc32.h
  - [ ] SDL_test_font.h
  - [ ] SDL_test_fuzzer.h
  - [ ] SDL_test_harness.h
  - [ ] SDL_test_images.h
  - [ ] SDL_test_log.h
  - [ ] SDL_test_md5.h
  - [ ] SDL_test_memory.h
  - [ ] SDL_test_random.h
- [ ] SDL_thread.h
- [x] SDL_timer.h
- [ ] SDL_touch.h
- [ ] SDL_types.h
- [ ] SDL_version.h
- [x] SDL_video.h
- [ ] SDL_vulkan.h
