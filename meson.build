project('3rdPartyPublic', ['cpp'], version : '0.0.1',
	default_options: ['prefix=@0@'.format(meson.current_source_dir() / 'stage')]
)
build_x64 = get_option('arch') == 'x64'

deps = []

if host_machine.system() == 'windows'  # These libraries only have windows binaries
	subdir('libdc1394-2.2.1-bin')
	subdir('pugixml-1.8')
	subdir('Thorlabs')
endif

'''
if host_machine.system() == 'linux'
	subdir('ITC18')
endif
'''