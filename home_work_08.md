1) Докеризовать приложение https://github.com/anestesia001/simple-docker-apps/tree/main/mock-api
2) Написать пайплайн, который при пуше в репозиторий:
    - собирает Docker-образ
    - запускает тесты\
    команда для запуска тестов
    ```
    pytest -v
    ```
    - пушит образ в registry (docker hub)
