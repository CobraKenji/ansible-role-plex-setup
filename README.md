# Ansible Plex
Install and configure Plex Media Server on CentOS/RHEL or Ubuntu/Debian.

### Plex configuration
```
plex_rpm_url: https://downloads.plex.tv/plex-media-server/1.1.4.2757-24ffd60/plexmediaserver-1.1.4.2757-24ffd60.x86_64.rpm # configure the rpm download URL
plex_deb_url: https://downloads.plex.tv/plex-media-server/1.1.4.2757-24ffd60/plexmediaserver_1.1.4.2757-24ffd60_amd64.deb  # configure the deb download URL
plex_deb_path: /tmp/plexmediaserver_1.1.4.2757-24ffd60_amd64.deb   # configure the deb download destination
plex_rpm_path: /tmp/plexmediaserver-1.1.4.2757-24ffd60.x86_64.rpm  # configure the rpm download destination

plexupdate_repo: https://github.com/mrworf/plexupdate   # plexudate repo
plexupdate_dest: /var/lib/plexmediaserver/plexupdate    # plexupdate destination

plexupdate_email: 'user@email.com'                      # username for plex.tv download
plexupdate_pass: 'password'                      		# password for plex.tv download
plexupdate_downloaddir: /tmp 							# directory to download plex updates to
plexserver: 127.0.0.1									# plex server IP/hostname
autoupdate: yes											# autoupdate plex?
autoinstall: yes										# autoinstall plex?
autodelete: yes											# autodelete after install?
public: no 												# use 'no' for plexpass download		
```

## Dependencies
None.

## Example Playbook
    - hosts: whatever
      become: yes
      roles:
        - plex