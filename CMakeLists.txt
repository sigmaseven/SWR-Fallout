cmake_minimum_required(VERSION 3.13)
project(SWR-Fallout)
set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 21)

set(SOURCE_FILES swr-fallout/src/act_comm.c
        swr-fallout/src/act_info.c
        swr-fallout/src/act_obj.c
        swr-fallout/src/act_move.c
        swr-fallout/src/act_wiz.c
        swr-fallout/src/boards.c
        swr-fallout/src/build.c
        swr-fallout/src/clans.c
        swr-fallout/src/comm.c
        swr-fallout/src/const.c
        swr-fallout/src/db.c
        swr-fallout/src/fight.c
        swr-fallout/src/handler.c
        swr-fallout/src/hashstr.c
        swr-fallout/src/id.c
        swr-fallout/src/interp.c
        swr-fallout/src/magic.c
        swr-fallout/src/makeobjs.c
        swr-fallout/src/misc.c
        swr-fallout/src/morespace.c
        swr-fallout/src/mud_comm.c
        swr-fallout/src/mud_prog.c
        swr-fallout/src/planets.c
        swr-fallout/src/player.c
        swr-fallout/src/requests.c
        swr-fallout/src/reset.c
        swr-fallout/src/save.c
        swr-fallout/src/shops.c
        swr-fallout/src/skills.c
        swr-fallout/src/smalloc.c
        swr-fallout/src/space.c
        swr-fallout/src/special.c
        swr-fallout/src/swskills.c
        swr-fallout/src/tables.c
        swr-fallout/src/track.c
        swr-fallout/src/update.c
        swr-fallout/src/vote.c)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY  ${PROJECT_SOURCE_DIR}/swr-fallout/bin)
add_executable(swr-fallout ${SOURCE_FILES})
target_include_directories(swr-fallout PUBLIC swr-fallout/src)
target_link_libraries(swr-fallout PUBLIC crypt m)
