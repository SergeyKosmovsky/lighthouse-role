# Role Lighthouse

Репа для установки программы Lighthouse в рамках ДЗ площадки netology

# Requirements

Centos8

# Role Variables

nginx_user_name - пользователь для запуска nginx;

lighthouse_archive - имя загружаемого zip-архива веб-приложения;

lighthouse_unzip_dir - директория для размещения zip-архива;

lighthouse_location_dir - directory to unzip the archive into;

lighthouse_access_log_name - имя лог-файла;

lighthouse_clh_access_point_file -  js-файл для замены значения db_host;

lighthouse_clh_access_point_regexp - регулярное выражение для распознавания строки db_host в js-файле;

lighthouse_clh_access_point - строка для установки db_host

db_host = 'http://{{ clickhouse_host_ip }}:8123/';


# Dependencies
ngix встроен в установку

# Example Playbook
  hosts: servers
  roles:
    - lighthouse_role
