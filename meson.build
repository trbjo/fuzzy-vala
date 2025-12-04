project('fuzzy-gnome', 'c')
project_name = 'io.github.trbjo.fuzzy-gnome'

inc = include_directories('src')

vapi_dir = meson.current_source_dir()

fuzzy_gnome_lib = static_library('fuzzy-gnome',
    sources: [
        'src/bonus.h',
        'src/config.h',
        'src/match.c',
        'src/match.h',
    ],
    include_directories: inc,
    install: false,
    c_args: ['-D_GNU_SOURCE'],
)

fuzzy_gnome_dep = declare_dependency(
    link_with: fuzzy_gnome_lib,
    include_directories: [inc, include_directories('.')],
    variables: {'vapi_dir': vapi_dir}
)
