current = meson.current_source_dir()
compiler = meson.get_compiler('cpp')

libName = 'libdc1394-22'

if build_x64
	dir = 'x64'
else
	dir = 'Win32'
endif
lib = compiler.find_library(libName, dirs: current / dir )

dep = declare_dependency(include_directories: 'include', dependencies: lib)
meson.override_dependency('libdc1394', dep)
install_data(current / dir / libName + '.dll')