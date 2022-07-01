# geekoops-mysql

Configurable ansible role for setting up mysql8. Works with

- openSUSE Leap 15.4

## Role Variables
--------------

 Value | Description | Default |
|-------|-------------|---------|
|`connect_timeout`| Number of seconds before connection timeout | 30 |
|`default_storage_engine`| Set the default storage engine | InnoDB |
|`innodb_flush_method`| Instructs InnoDB on how to open and flush log and data files | fsync |
|`tmp_table_size`| Size of a temporary table | 32M |
|`max_heap_table_size`| Maximum size of user-created memory tables are permitted to grow | 32M |
|`innodb_buffer_pool_size`| Size of the buffer pool, the memory area where InnoDB caches table and index data. | 2048M |
|`thread_cache_size`| Number of threads the server should cache for reuse. | 16 |

## Example Playbook

Including an example of how to use the role:

    - hosts: jellyfish
      user: root
      roles:
        - role: geekoops-mysql
      vars:
        connect_timeout: 30
        default_storage_engine: InnoDB
        innodb_flush_method: fsync
        tmp_table_size: 32M
        max_heap_table_size: 32M
        innodb_buffer_pool_size: 2048M
        thread_cache_size: 16

## License

MIT
