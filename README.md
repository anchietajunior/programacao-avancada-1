# Programação Avançada - Projeto exemplo

## Gerar um novo projeto Rails

```shell
rails new meu_projeto -j esbuild -c tailwind -T --skip-jbuilder
```

## Configurando o projeto para executar com bin/dev.bat

1 - Crie um arquivo `dev.bat` na pasta `bin`

2 - Adicione o seguinte conteúdo:

```
@echo off
foreman start -f Procfile.dev
```

3 - Modifique o arquivo Procfile.dev para:

```
web: env RUBY_DEBUG_OPEN=true rails server
js: yarn build --watch
css: yarn build:css --watch
```

4 - Executando o projeto bin/dev.bat
