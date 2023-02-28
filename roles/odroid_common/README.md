odroid_common
=============

A simple role to handle tasks common to a lot of Hardkernel Odroid configuration. Currently that just consists of the LED trigger configuration.

Requirements
------------

None known, other than running on an Odroid machine with a recent kernel and userspace.

Role Variables
--------------

* odroid_led_trigger: The event to trigger the heartbeat LED on. Defaults to 'sd'. Could often be 'mmc0', 'sd' and others.

Dependencies
------------

None.

Example Playbook
----------------

```yaml
---
- name: Odroid nodes
  hosts: odroid
  vars:
    odroid_led_trigger: mmc0
  roles:
    - odroid_common
```

License
-------

Apache-2.0

Author Information
------------------

