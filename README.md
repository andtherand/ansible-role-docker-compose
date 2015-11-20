# Ansible docker-compose role

This is a simple role that facilitates the mighty docker-compose.
It's by nomeans perfect, but satisifies my current needs to create dependent docker containers in a more dynamic way using the aforementioned docker-compose.

## Requirements

You need to have docker and docker-compose (I guess docker.py) installed.

## Role variables

The following variables are available:

```
docker_compose_src_template: /path/to/docker-compose_my_template.yml.j2
```
It sets the path to a docker-compose template file. The path can be anywhere, and is not bound to the relative location of the role.
Due to the nature, this variable has no default value and has to be set.

```
docker_compose_dest: /my/remote/destination/path
```
Sets the destination path on the machine that's provisioned. Also this variable has no default value because it depends on your specifics.

```
docker_compose_file: my-docker-compose.yml # default: docker-compose
```
The docker-compose file to be used by ```docker-compose -f {{ docker_compose_file }} [up | stop | rm]```

```
docker_compose_rebuild_images: no # default: no
```
Force stop container and removal.

## Tags

This role makes vivid use of tags.
The following tags are available:

- docker-compose
- docker-compose-up
- docker-compose-stop
- docker-compose-rm
- docker-compose-rebuild-images
- docker-compose-template
- debug

## Example playbook

TODO: Make example ;)

A working example can be found at mychiara/ansible-docker-compose-example.

```
```

## Contributing

In lieu of a formal styleguide, take care to maintain the existing coding style. Would be create if you added unit tests, that's on my todo list aswell :]

1. Fork it
2. Create your feature branch (git checkout -b feature/my-cool-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin feature/my-new-feature)
5. Create new Pull Request

## License

Copyright (c) mychiara | svs under the GPLv2 license.