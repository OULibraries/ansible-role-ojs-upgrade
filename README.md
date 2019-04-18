OULibraries.ojs-upgrade
=========

Open Journal Systems for OU Libraries

Requirements
------------

Existing OJS Installation Utilizing:
- NGINX
- MySQL
- PHP

Role Variables
--------------

- sclphp_version: Required SCLPHP version (IE: rh-php70), will upgrade if needed
- ojs_version: The target version number
- ojs_parent_dir: Base Apache/HTTPD Site Directory 
- ojs_md5sum: Checksum for OJS Tarball
- ojs_download_url: Base URL for OJS Tarball

Dependencies
------------


```
- src: https://github.com/OULibraries/ansible-role-ojs
  version: master
  name: OULibraries.ojs
- src: https://github.com/OULibraries/sclphp
  version: master
  name: OULibraries.sclphp
```

Example Playbook
----------------
```
    - hosts: servers
      roles:
         - role: OULibraries.sclphp
           tags: sclphp
         - role: OULibraries.ojs-upgrade
           tags: ojs-upgrade
````

License
-------

[MIT](https://github.com/OULibraries/ansible-role-ojs-upgrade/blob/master/LICENSE)

Author Information
------------------
Cody Bennett
Jason Sherman
Logan Cox
