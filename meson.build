project(
  'light',
  'c',
  version: '1.2.0',
  license: 'MIT',
  meson_version: '>=0.60.0',
  default_options: [
    'c_std=c11',
    # 'warning_level=2',
    # 'werror=true',
    ],
)

add_project_arguments(
  [],
  language: 'c',
)

cc = meson.get_compiler('c')

version = meson.project_version()

add_project_arguments('-D_GNU_SOURCE', '-DVERSION="' + version + '"', language : 'c')

light_inc = include_directories('include')
conf_data = configuration_data()

subdir('include')
subdir('src')
