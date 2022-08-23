# inventorio

inventorio is an inventory application to track data using a simple [tag system](#Tag System).
You can manage this data in multiple ways, such as:

- Web GUI
- API
- CLI

The original intent of this application is to be used as an [Ansible Dynamic Inventory Source](https://docs.ansible.com/ansible/latest/user_guide/intro_dynamic_inventory.html).
If it seems useful to you in other contexts, feel free and adopt it to your needs.

## Installation

TODO

## Usage

TODO

## Tag System

inventorio uses a simple text-based tag system consisting of `entry`s and `tag`s.
An `entry` is a single text field. Each `entry` has 0 or many `tag`s.
A `tag` has a `name` and `value`.

```text
                           Entry
                      -----------------
                      | name: node001 |
                      -----------------
                        |           |
             Tag        |           |       Tag
-----------------------------   -----------------------------
| name: ip_address_external |   | name: ip_address_internal |
| value: 1.2.3.4            |   | value: 10.1.1.1           |
-----------------------------   -----------------------------
```
