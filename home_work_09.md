Написать пайплайн для деплоя приложения https://github.com/anestesia001/simplest-todo/tree/main
- прогон линтера
```yaml
image: registry.gitlab.com/pipeline-components/php-linter:latest
  script:
    - parallel-lint --colors .
```
- прогон тестов командой
```bash
composer init -n  # если ещё нет composer.json
composer require --dev phpunit/phpunit
./vendor/bin/phpunit tests/TodoAppTest.php
```
- сборка docker image и push его в docker hub
- деплой на удаленную машину в ручном режиме
