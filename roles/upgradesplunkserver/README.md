upgradesplunkserver
===================

A quick upgrade for Splunk server role.

Requirements
------------

A Splunk server running on Ubuntu, the latest Splunk DEB package, and a text editor to edit a variable file (splunk-server-version.yml).

You will need to:
   * Download the latest Splunk server DEB package
   * Copy that package into the /files/ directory
   * Edit the file /vars/splunk-server-version.yml and include
     the new version and build numbers from the file DEB package name.

Role Variables
--------------

The splunkserverversion variable in vars/splunk-server-version.yml contains the version and build number for the Splunk package. It is used to test if the latest version of Splunk is already installed, and finding the package name. 

Dependencies
------------

None.

Example Playbook
----------------

```yml
- hosts: serversplunk
  become: true
  roles:
    - upgradesplunkserver
```


License
-------

BSD

Author Information
------------------

Troy Johnson
troy@jdmz.net
http://troy.jdmz.net/

