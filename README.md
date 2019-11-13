# Ambiente Docker teste com PHP 7.4-fpm, Xdebug,  Nginx e MySQL 8 

Para executar:

`git clone https://github.com/gilbertoalbino/php74-fpm-docker.git`

`cd php74-fpm-docker/docker`

`docker-compose up -d`

## Importante ##

Se as portas __80__ e __3306__ estiverem em uso, no arquivo `docker/docker-compose.yml` mude para algo como:
```
  nginx:
    ...
    ports:
      - "8080:80"
      - "4430:443"

  mysql:
    ...
    ports:
      - "33060:3306"
```

Ou para alguma outra combinação de portas abertas no seu sistema operacional.

Abra o navegador em __http://localhost__ e pronto!

Você deverá ver a tela do `phpinfo()`.

Daí pra frente espero que você saiba o que fazer! :P





