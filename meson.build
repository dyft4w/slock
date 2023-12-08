# Name, Language
project('slock','c')
version='1.5'
# Files
src=['slock.c','explicit_bzero.c']
# Dependencies (x11, xfreetype)
x11_dep = [dependency('x11'),dependency('xext'),dependency('libcrypto'),dependency('xrandr')] #,dependency('freetype2'),dependency('xft'),dependency('fontconfig')]
#others (ugly ahh hell ik ik), Wno-d-d is in the OG Makefile
add_project_arguments(['-DVERSION="'+version+'"','-Wall','-pedantic'],language : 'c')
add_project_link_arguments(['-lcrypt','-lc'],language:'c')
install='/usr/local/bin/'
optimization='s'
executable('slock',
            src,
            dependencies : x11_dep,
            install : true,
            install_dir : install)
install_man('slock.1')
