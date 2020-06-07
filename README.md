# Readme

Importante criar as entradas no banco mysql após subir o container do mysql.

Para isso, entrar no container:
```
$ docker exec -it "nome do container" bash
# mysql -u root
# create table produtos (id integer auto_increment primary key, nome varchar(255), preco decimal(10,2));
# alter table produtos add column usado boolean default false;
# alter table produtos add column descricao varchar(255);
# create table categorias (id integer auto_increment primary key, nome varchar(255));
# insert into categorias (nome) values ("Futebol"), ("Volei"), ("Tenis");
# alter table produtos add column categoria_id integer;
# update produtos set categoria_id = 1;

```

Após isso, rodar o compose down e up novamente:
```
$ docker-compose down --volumes
$ docker-compose up --build

```

Testar a aplicação php na porta especificada...

# OBS.: Criação da image

Fizemos o push da imagem da aplicacao no dockerhub, por isso alteramos no docker-compose para apontar para o dockerhub e não para o build local.

Mas temos q lembrar q antes de fazer o upload para o dockerhub, foi feito o build local da imagem da aplicação...

