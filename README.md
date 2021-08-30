# cpfcnpj-compose
Aplicação que cria o ambiente em docker das aplicações:
- server: https://github.com/renanbet/cpfcnpj-server
- client: https://github.com/renanbet/cpfcnpj-client

## Pré-requisitos

- git
- docker
- docker-compose


## Ambiente linux

- Clonar o repositório
```
git clone https://github.com/renanbet/cpfcnpj-compose.git
git checkout master
```

- Atribuir permissão de execução para o cli.sh
```
chmod 777 cli.sh
```

- Instalar o client e server
```
./cli.sh setup
```

- Subir os ambientes
```
make up
```
ou
```
docker-compose up -d
```

- Buildar os ambientes (na primeira vez do up já é buildado)
```
make build
```
ou
```
docker-compose build --no-cache
```

## Acessar a aplicação

```
http://localhost:8080
```

## Logs

- Para ver todos os logs
```
make logs
```
ou
```
docker-compose logs -f
```

## Para parar aplicações

```
make down
```
ou
```
docker-compose down
```

## Testes
```
cd tests
make up
make logs
ou
docker-compose logs cpfcnpjapitest
docker-compose logs cpfcnpjclienttest
```
