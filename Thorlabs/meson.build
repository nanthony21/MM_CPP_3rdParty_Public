current = meson.current_source_dir()
compiler = meson.get_compiler('cpp')
#### KURIOS ####
SDK_dir = 'Kurios-C++SDKv1.6.2'

if build_x64
	libName = 'KURIOS_COMMAND_LIB_Win64'
else
	libName = 'KURIOS_COMMAND_LIB_Win32'
endif

deps = [
	compiler.find_library(libName, dirs: current / SDK_dir),
]

includes = [
	SDK_dir
]


SDK_dep = declare_dependency(include_directories: includes, dependencies: deps, version: '1.6.2')
meson.override_dependency('KuriosSDK', SDK_dep)
install_data(SDK_dir / libName + '.dll')