# CI/CD With Heroku


Este é um mini projeto de WebServices Rest para configuração do CI/CD no Heroku, a intenção é simplesmente ter um repositorio com esses conceitos, caso seja preciso reutilizar futuramente.

# Passo a passo
- Criando projeto no Heroku, provisionar Postgres e instanciar base de dados.

  Acesse o site: https://www.heroku.com/

  Em seguida crie o projeto clicando em "New", conforme a imagem abaixo:

  ![image](https://user-images.githubusercontent.com/100853329/179603721-b9948560-eadb-4448-8584-34c96f232414.png)

  Após isso é só configurar o projeto de acordo com sua preferência.
  
  Para associar um bando de dados, cliquem em "Resources" e digite na barra de pesquisa "Heroku Postgres"
  
  ![image](https://user-images.githubusercontent.com/100853329/179604148-b84fcd9e-7532-429d-aad8-11c448f525d8.png)

- Associando o projeto local ao Github e ao Heroku

  heroku -v
  
  heroku login
  
  heroku git:remote -a <nome-do-app>

  git remote -v

- Arquivo system.properties

  java.runtime.version=11

- Configurar variáveis de ambiente no Heroku

  APP_PROFILE

  CLIENT_ID

  CLIENT_SECRET

  JWT_SECRET

  JWT_DURATION

  DB_URL

  DB_USERNAME

  DB_PASSWORD

- Realizar deploy

  - Repositório comum:

    git push heroku main

  - Monorepositório (subpasta):

    git subtree push --prefix backend heroku main

# Testes

Link deste repositorio no Heroku: https://ajdeploy-heroku.herokuapp.com/

Collection do Postman para teste: https://www.getpostman.com/collections/57b3db0ca631de797502

Obs: No postman, você deve colar o link do heroku acima no lugar das chaves chamadas {{host}}, caso contrario, o end-point não irá trazer nenhum resultado.
