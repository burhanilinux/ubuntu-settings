project('ubuntu-default-launchers')

i18n = import('i18n')
subdir('po')
subdir('data/raspberrypi')

datadir = get_option('datadir')
installdir = join_paths(datadir, 'ubuntu-web-launchers')

desktop_file = 'gnome-initial-setup.desktop'
i18n.merge_file(input: 'data/ubuntu/applications/' + desktop_file + '.in',
                output: desktop_file,
                po_dir: 'po',
                install: true,
                install_dir: join_paths(datadir, 'ubuntu', 'applications'),
                type: 'desktop'
               )
install_data('data/ubuntu/applications/info.desktop',
              install_dir: datadir+'/ubuntu/applications/')
install_data('data/ubuntu/applications/texdoctk.desktop',
              install_dir: datadir+'/ubuntu/applications/')
foreach dir : ['data/ubuntu-wayland', 'data/icons']
        install_subdir(dir, install_dir: datadir)
endforeach
