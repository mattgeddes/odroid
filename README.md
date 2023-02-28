# Ansible Collection - mattgeddes.odroid

## Example Playbook

```yaml
---
- name: Odroid nodes
  hosts: odroid
  vars:
    odroid_led_trigger: sd
  roles:
    - odroid-common
```

## Roles

### odroid-common

A role to manage configuration common to most/all models of Odroid node. This includes:

 * Management of the LED trigger

Variables include:
 * `odroid_led_trigger` -- defaults to `sd`. Sets the trigger for the blue LED present in many models of Odroid SBC. See the contents of the `odroid_led_path` file for possible alternate values.
 * `odroid_led_path` -- defaults to `/sys/class/leds/blue:heartbeat/trigger`. The sysfs path used to control the LED trigger.

