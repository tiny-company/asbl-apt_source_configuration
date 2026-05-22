# asbl-apt_source_configuration

## Description

This repo contain the ansible role that configure apt sources :
- configure apt source repo.

## Prerequisite

- None

## Usage

### Use role

- Add the role git source in "requirements.yml" file :
```
  - name: role_name
    scm: git
    src: https://github.com/tiny-company/<repository_name>.git
    version: main
```

- And then use the galaxy command to load the file dependencies :
```
ansible-galaxy install -r requirements.yml
```

- Or manually get the playbook as collection (with ansible-galaxy) :
```
ansible-galaxy collection install https://github.com/tiny-company/<repository_name>.git
```

- finally use role in playbook : [see test_playbook example](./test_playbook.yml)

### Variables

For an exhaustive list of variables check the [defaults](./defaults/main.yml)
file. Ideally, all values will have commentaries describing what are their
purposes and by the default value you can tell the type.

## Source :

- [apt_key module](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/apt_key_module.html)

