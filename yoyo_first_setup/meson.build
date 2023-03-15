pkgdatadir = join_paths(get_option('prefix'), get_option('datadir'), meson.project_name())
moduledir = join_paths(pkgdatadir, 'yoyo_first_setup')
gnome = import('gnome')

gnome.compile_resources('yoyo-first-setup',
  'yoyo-first-setup.gresource.xml',
  gresource_bundle: true,
  install: true,
  install_dir: pkgdatadir,
)

python = import('python')

conf = configuration_data()
conf.set('PYTHON', python.find_installation('python3').path())
conf.set('VERSION', meson.project_version())
conf.set('localedir', join_paths(get_option('prefix'), get_option('localedir')))
conf.set('pkgdatadir', pkgdatadir)

configure_file(
  input: 'yoyo-first-setup.in',
  output: 'yoyo-first-setup',
  install_mode: 'rwxr-xr-x',
  configuration: conf,
  install: true,
  install_dir: get_option('bindir')
)

configure_file(
  input: 'yoyo-first-setup-processor.in',
  output: 'yoyo-first-setup-processor',
  configuration: conf,
  install: true,
  install_dir: get_option('bindir')
)

subdir('utils')
subdir('defaults')
subdir('layouts')
subdir('views')

yoyo_first_setup_sources = [
  '__init__.py',
  'main.py',
  'window.py',
  'dialog.py',
]

install_data(yoyo_first_setup_sources, install_dir: moduledir)