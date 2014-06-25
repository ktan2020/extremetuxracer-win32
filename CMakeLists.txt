cmake_minimum_required (VERSION 2.6)
project (etr)

add_definitions(-DOS_WON32_MINGW -D_GNU_SOURCE=1 -Dmain=SDL_main)

link_directories(/usr/local/lib)

add_executable(etr Audio.cpp common.cpp config_screen.cpp course.cpp course_render.cpp credits.cpp env.cpp event.cpp event_select.cpp font.cpp ft_font.cpp game_config.cpp game_ctrl.cpp game_over.cpp game_type_select.cpp gui.cpp help.cpp hud.cpp intro.cpp keyframe.cpp loading.cpp main.cpp mathlib.cpp newplayer.cpp ogl.cpp ogl_test.cpp particles.cpp paused.cpp physics.cpp quadtree.cpp race_select.cpp racing.cpp regist.cpp reset.cpp score.cpp splash_screen.cpp spx.cpp states.cpp textures.cpp tool_char.cpp tool_frame.cpp tools.cpp track_marks.cpp translation.cpp tux.cpp view.cpp winsys.cpp)

target_link_libraries(etr SDL SDL_image SDL_mixer SDLmain freetype opengl32 glu32)