# nginx

Установка nginx. Копирование конфигурационных файлов.

## Пример использования

```bash
- role: nginx
      nginx_default: false
      nginx_vhosts:
        - name: 1039922325-students.devboxops.xyz
          nginx_conf: nginx_conf.j2
          le_cert_renewal: true
          cert_type: LE
```

## Доступные параметры

Параметр| Значение по умолчанию|Описание
 --- | --- | ---
nginx_default|true|Использовать ли стандартные конфигурации (boolean)
nginx_vhosts|-|Список переменных виртуальных хостов (list)
name|-|Имя виртуального хоста (str)
nginx_conf|-|Путь к шаблону конфигурационного файла фиртуального хоста (str)
html_conf|-|Путь к стартовой html-странице (str)
le_cert_renewal|false|Необходимо ли перевыпустить LE сертификат (boolean)
cert_type|-|Тип сертификата (str). Принимает значения LE, CS