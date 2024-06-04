project('ht', 'c',    meson_version: '>=1.4.0')

# Declare the source files
ht_sources = files('ht.c')

# Include directories
ht_include = include_directories('.')

# Create a static library
ht_lib = static_library('ht', ht_sources,
                        include_directories: ht_include,
                        install: true)

# Install the library and headers
install_headers('ht.h')
install_targets(ht_lib)

# Expose variables to the main project
ht_lib_dep = declare_dependency(link_with: ht_lib, include_directories: ht_include)

# Set these variables to be accessible by the parent project
htlib_dep = ht_lib_dep
htlib_inc = ht_include
