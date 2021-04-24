current = meson.current_source_dir()
compiler = meson.get_compiler('cpp')

lib = static_library('pugixml', sources: ['src' / 'pugixml.cpp'], include_directories: ['src'], version: '1.8')

dep = declare_dependency(include_directories: 'src', libraries: lib)
meson.override_dependency('pugixml', dep)
