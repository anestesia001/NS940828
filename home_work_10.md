Написать пайплайн gitlab ci для приложения https://github.com/anestesia001/dos-36-glab-01

Требования к пайплайну
1) Состоит из этапов
```
build
test
deploy
check
```
2) Пуш собранного docker image в docker hub с двумя тегами: latest и CI_COMMIT_SHORT_SHA
3) Деплой осуществляется на **удаленную** машину в ручном режиме (`manual`)
