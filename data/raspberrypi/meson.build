etc = get_option('sysconfdir')
var_lib = get_option('sharedstatedir')

install_data('10-raspi-eth0.link',
             install_dir: 'lib/systemd/network')
install_data('ZZraspi-wifi-powersave-off.conf',
             install_dir: 'lib/NetworkManager/conf.d')
install_data('disable-suspend.pkla',
             install_dir: var_lib / 'polkit-1/localauthority/10-vendor.d')
install_data('99-gpio.rules',
             install_dir: 'lib/udev/rules.d')
install_data('raspi-lz4.conf',
             install_dir: etc / 'initramfs-tools/conf.d')
