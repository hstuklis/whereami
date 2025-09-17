project(
  'whereami',
  'c',
  license: 'MIT',
  default_options: ['c_std=c11', 'warning_level=3', 'default_library=static'],
  meson_version: '>=1.1',
)
whereami_include_dir = include_directories('src')
whereami_lib = library(
    'whereami',
    'src/whereami.c',
    include_directories: whereami_include_dir,
    install: true,
)
whereami_dep = declare_dependency(
  link_with: [whereami_lib],
  include_directories : whereami_include_dir
)
meson.override_dependency('whereami', whereami_dep)