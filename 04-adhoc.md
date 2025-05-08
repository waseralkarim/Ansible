# Adhoc:

**Ad-hoc commands** are one-liner commands used to perform quick, immediate tasks on managed hosts without writing a full playbook. They are especially useful for testing, debugging, or small-scale administrative tasks.

Running some Ansible Ad-hoc Commands:

- i = location, -m = module, -a = argument

For all control nodes:

```bash
ansible -i <.INI FILE LOCATION> -m ping all
```

```bash
ansible -i <.INI FILE LOCATION> -m shell -a “apt install openjdk” all”
```

For specific control node:

```bash
ansible -i <.INI FILE LOCATION> -m ping <hostname>@<ip add>
```

If the host is not in the inventory it will show an error.

**For grouping method:**

Inventory will look like:

```bash
[app]

<hostname>@<ip_add>

[db]

<hostname>@<ip_add>
```

```bash
ansible -i <.INI FILE LOCATION> -m ping db
```
