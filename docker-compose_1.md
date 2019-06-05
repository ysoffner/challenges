New Way Labs
============
## Stack Web utilizando Docker && docker-compose

### Objetivo:
* Construir um ambiente de desenvolvimento em **Laravel**, dentro to container PHP, é necessario copiar seu projeto local para o diretorio **/app**, instalar as dependencias dentro do container PHP (composer, libs, ...) e buildar o composer.json.
* Expor a porta do container no Dockerfile, habilitando assim, o acesso externo
* Na configuração do Nginx, temos que mudar o **location /** e apontar o container do php para ser intepretado a extensão _.php_

##### Requisitos:
* Dockerfile para cada serviço.
* Configurar as variáveis de ambiente necessárias.
* Volumes persistentes.
* 2 Networks, backend e frontend.

##### Serviços:

| Serviço | Porta | versão |
|-------|--------|---|
|php|9001|7.0|
|nginx|8080|alpine_latest|
|mysql|3306|8|
|mongo|27017|4.1.11|
|redis|6379|5.0.5|
