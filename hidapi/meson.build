current = meson.current_source_dir()
compiler = meson.get_compiler('cpp')
#### HIDAPI ####

if build_x64
	arch_dir = 'x64'
else
	arch_dir = 'x86'
endif

deps = [
	compiler.find_library('hidapi', dirs: current / arch_dir),
]



SDK_dep = declare_dependency(include_directories: ['.'], dependencies: deps, version: '0.10.1')
meson.override_dependency('hidapi', SDK_dep)
install_data(arch_dir / 'hidapi.dll')