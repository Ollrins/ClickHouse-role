# Ansible Role: Сlickhouse

Устанавливает ClickHouse из RPM пакетов.

## Требования

- ОС: Rocky Linux / RHEL 8+
- Ansible 2.9+
- Архитектура: x86_64

## Переменные

| Параметр | Описание | Значение по умолчанию |
|----------|----------|----------------------|
| `clickhouse_version` | Версия ClickHouse для установки | `24.8.13.16` |

### Доступные версии

Версии можно посмотреть по ссылке:  
https://packages.clickhouse.com/rpm/stable/

Примеры доступных версий:
- `24.8.13.16`
- `24.8.14.39`
- `24.9.1.3278`
- `24.10.1.2812`

## Dependencies

Нет зависимостей от других ролей.

## Example Playbook

```yaml
- hosts: clickhouse
  become: true
  roles:
    - role: clickhouse
      vars:
        clickhouse_version: "24.8.14.39"
