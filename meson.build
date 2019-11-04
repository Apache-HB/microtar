project('microtar', 'c',
    version : '1.0',
    license : 'rxi'
)

source = 'src/microtar.c'
header = 'src/microtar.h'

incdir = include_directories('src')

tar_lib = static_library('tar', source, include_directories : incdir, install : true)
tar_dep = declare_dependency(link_with : tar_lib, include_directories : incdir)

pkg = import('pkgconfig')
pkg.generate(tar_lib, name : 'microtar', description : 'A lightweight tar library written in ANSI C')
