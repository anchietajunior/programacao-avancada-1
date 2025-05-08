# Programação Avançada - Projeto exemplo

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