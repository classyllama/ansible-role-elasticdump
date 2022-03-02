# Ansible Role: ElasticDump utility

Installs 'elasticdump' utility for dumping/restoring ElasticSearch indices. It requires nodejs installed on the server.

## Requirements

    use_classyllama_repo_nodesource: true

## Role Variables

    use_classyllama_elasticdump: true|false

## Dependencies

     - { role: classyllama.repo-nodesource, tags: nodejs, when: use_classyllama_repo_nodesource | default(false) }

## Example Playbook

    - hosts: all
      roles:
         - { role: classyllama.elasticdump, tags: elasticdump, when: use_classyllama_elasticdump | default(false) }

## Notes

Please visit https://github.com/elasticsearch-dump/elasticsearch-dump for usage information

## License

This work is licensed under the MIT license. See LICENSE file for details.
