# Para iniciar um novo projeto:
~~~
💲 rails new nome_do_projeto #inicia com o BD original do Rails, vulgo SQLite
~~~
~~~
💲 rails new nome_do_projeto --database mysql

 #inicia com o BD mysql, postgresql, etc
~~~

+ Acesse a pasta com o nome do projeto pelo terminal e:
~~~
💲 rails server

💲 rails s
~~~
*para levantar o servidor*

+ Acesse a aplicação em **http://localhost:3000/**

# Criando a página inicial do seu projeto:
~~~
💲 rails g controller welcome index
~~~
*isso cria um controller chamado WELCOME com uma ação INDEX*

# Indicando a rota incial para a página inicial criada:

+ No arquivo 📂**config/routes.rb**:
~~~
root to: 'welcome#index'
~~~
