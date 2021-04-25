current = meson.current_source_dir()
compiler = meson.get_compiler('cpp')

lib = static_library('pugixml', sources: ['src' / 'pugixml.cpp'], include_directories: ['src'])

dep = declare_dependency(include_directories: 'src', link_with: lib,  version: '1.8')
meson.override_dependency('pugixml', dep)
