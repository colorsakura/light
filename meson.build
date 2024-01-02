project(
  'light',
  'c',
  version: '1.3.0-dev',
  license: 'MIT',
  meson_version: '>=0.60.0',
  default_options: [
    'c_std=c11',
    # 'warning_level=2',
    # 'werror=true',
    ],
)

cc = meson.get_compiler('c')

version = meson.project_version().split('-')[0]

add_project_arguments('-D_GNU_SOURCE', '-DVERSION="' + version + '"', language : 'c')

install_man(
  'man/light.1'
)

light_inc = include_directories('include')
conf_data = configuration_data()

subdir('include')
subdir('src')
