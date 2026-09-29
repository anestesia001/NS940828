Для приложения https://github.com/anestesia001/dos-36-glab-02 создать пайплайн со следующими этапами
1) **build:**
    - Сборка Docker-образа приложения
    - Push образа в Docker Hub
2) **test:**
    - Запуск тестов в матрице параллельных джоб:
      - Python версии: 3.9, 3.10, 3.11
      - ОС: ubuntu, alpine
3) **deploy (Downstream Pipeline):**
  - Триггер downstream pipeline для деплоя
  - Downstream pipeline должен:
      - Разворачивать приложение на удаленной машине
      - Выполнять smoke-тесты после деплоя
