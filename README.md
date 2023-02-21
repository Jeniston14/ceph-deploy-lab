# ceph-deploy-lab

uuidgen для генерации fsid

Keyring create mon

ceph-authtool --create-keyring /tmp/ceph.mon.keyring --gen-key -n mon. --cap mon 'allow +'

creating /tmp/ceph.mon.keyring


Keyring create admin

ceph-authtool --create-keyring /etc/ceph/ceph.client.admin.keyring --gen-key -n client.admin --cap mon 'allow *' --cap osd 'allow *' --cap mds 'allow *' --cap mgr 'allow *'

creating /etc/ceph/ceph.client.admin.keyring


Keyring bootstrap osd

ceph-authtool --create-keyring /var/lib/ceph/bootstrap-osd/ceph.keyring --gen-key -n client.bootstrap-osd --cap mon 'profile bootstrap-osd' --cap mgr 'allow r'

creating /var/lib/ceph/bootstrap-osd/ceph.keyring
