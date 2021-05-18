current = meson.current_source_dir()
compiler = meson.get_compiler('cpp')
#### KURIOS ####
SDK_dir = '3.1.4'

if build_x64
	libDir = 'win64'
else
	libDir = 'win32'
endif

deps = [
	compiler.find_library('modbus', dirs: current / SDK_dir / libDir),
]

includes = [
	SDK_dir / libDir
]


SDK_dep = declare_dependency(include_directories: includes, dependencies: deps, version: '3.1.4')
meson.override_dependency('modbus', SDK_dep)
install_data(SDK_dir / libDir / 'modbus.dll')